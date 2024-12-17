<!-- @format -->
<script lang="ts" module>
  import Command from "lucide-svelte/icons/command";
  import Users from "lucide-svelte/icons/users";
  import * as Collapsible from "$lib/components/ui/collapsible/index.js";
  import ChevronRight from "lucide-svelte/icons/chevron-right";

  let items: {
    title: string;
    url: string;
    // this should be `Component` after lucide-svelte updates types
    // eslint-disable-next-line @typescript-eslint/no-explicit-any
    icon?: any;
    isActive?: boolean;
    items?: {
      title: string;
      url: string;
    }[];
  }[];
  // sample data
  const data = {
    versions: ["Devii.io"],
    navMain: [
      {
        title: "Events Overview",
        url: "/",
        icon: Command,
      },
    ],
  };

  items = data.navMain;
</script>

<script lang="ts">
  import VersionSwitcher from "$lib/components/version-switcher.svelte";
  import * as Sidebar from "$lib/components/ui/sidebar/index.js";
  import type { ComponentProps } from "svelte";

  let {
    ref = $bindable(null),
    collapsible = "icon",
    ...restProps
  }: ComponentProps<typeof Sidebar.Root> = $props();
</script>

<Sidebar.Root {...restProps} bind:ref {collapsible}>
  <Sidebar.Header>
    <VersionSwitcher
      versions={data.versions}
      defaultVersion={data.versions[0]}
    />
  </Sidebar.Header>
  <Sidebar.Content>
    <!-- We create a Sidebar.Group for each parent. -->
    <Sidebar.Group>
      <Sidebar.GroupLabel>Platform</Sidebar.GroupLabel>
      <Sidebar.Menu>
        {#each items as mainItem (mainItem.title)}
          <Sidebar.MenuItem>
            <Sidebar.MenuButton>
              <a href={mainItem.url} class="flex items-center gap-2">
                {#if mainItem.icon}
                  <mainItem.icon />
                {/if}
                <span>{mainItem.title}</span>
              </a>
            </Sidebar.MenuButton>
          </Sidebar.MenuItem>
        {/each}
      </Sidebar.Menu>
    </Sidebar.Group>
  </Sidebar.Content>
  <Sidebar.Rail />
</Sidebar.Root>
