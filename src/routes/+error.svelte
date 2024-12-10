<!-- @format -->
<script>
  import { page } from "$app/stores";
  import error404 from "$lib/components/errors/404.svelte";
</script>

{#if $page.status === 404}
  <svelte:component this={error404} />
{/if}
