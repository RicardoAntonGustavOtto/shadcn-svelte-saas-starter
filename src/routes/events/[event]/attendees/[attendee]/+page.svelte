<!-- @format -->
<script lang="ts">
  import { page } from "$app/stores";
  import { onMount } from "svelte";
  import { updateBreadcrumbs } from "$lib/stores/breadcrumbs.js";
  import { Badge } from "$lib/components/ui/badge";
  import EditIcon from "lucide-svelte/icons/pencil-line";
  import CompanyIcon from "lucide-svelte/icons/building-2";

  // Define variables for the slugs
  let eventId: string | null = null;
  let attendeeSlug: string | null = null;

  // Reactive statement to derive slugs from the page store
  $: {
    const { params } = $page; // Use $page to access the current page's parameters
    eventId = params.eventId || null; // For routes like /events/[eventId]/attendees/[attendee]
    attendeeSlug = params.attendee || null; // For routes like /events/[eventId]/attendees/[attendee]
  }

  onMount(() => {
    // Update breadcrumbs with the derived slugs
    updateBreadcrumbs(eventId, attendeeSlug);
  });

  let retzer = {
    url: "https://www.linkedin.com/in/retzer/",
    social_activity: [
      {
        post_url:
          "https://www.linkedin.com/feed/update/urn:li:activity:7260045432519634945",
        nb_comments: 2,
        nb_likes: 48,
        reacted: "LIKE",
        date: "2024-11-06 21:48:36.234000",
        days_from_today: 28,
        timestamp: 1730929716.234,
      },
    ],
    about:
      "Experienced Senior Sales Executive with extensive experience in the aviation and software industries.",
    education: [
      {
        months_duration: "",
        start_date: "1992",
        end_date: "1996",
        description: "",
        title: "Kalamazoo College",
        company: "BA, Economics",
        company_linkedin: "https://www.linkedin.com/company/20115/",
        location: "",
      },
      {
        months_duration: "",
        start_date: "1988",
        end_date: "1992",
        description: "",
        title: "Fargo South High School",
        company: "Diploma , General Studies",
        company_linkedin: "",
        location: "",
      },
    ],
    languages: [
      {
        language: "English",
        level: "Native or bilingual proficiency",
      },
      {
        language: "German",
        level: "Native or bilingual proficiency",
      },
    ],
    volunteer: [],
    location: "Bonn, North Rhine-Westphalia, Germany",
    premium: true,
    influencer: "",
    creator: "",
    profile_picture:
      "https://media.licdn.com/dms/image/v2/C4E03AQH3GcdMXe3eBg/profile-displayphoto-shrink_400_400/profile-displayphoto-shrink_400_400/0/1596560909039?e=1738800000&v=beta&t=tLWkG0h65np1hlsmqVI8VXEoL9_vr3Tud6yU0UGqeqk",
    profile_picture_expiresAt: "06-02-2025",
    profile_picture_type: "ORIGINAL",
    profile_picture_saturation: "0.0",
    profile_picture_brightness: "0.0",
    profile_picture_contrast: "0.0",
    pronoun: "",
    creator_hashtags: [],
    creator_website: {
      text: "",
      link: "",
    },
    account_created_at: "05-10-2024",
    phonenumbers: ["+491718438999"],
    email: "rick.retzer@gmail.com",
    lastName: "Retzer",
    firstname: "Rick",
    headline: "SalesSpaice - Close more deals",
    birthday_ddmm: "13-01",
    social_accounts: {},
    websites: [],
    followers: 1416,
    connections: 1421,
    experience: [
      {
        months_duration: "6",
        start_date: "07-2024",
        end_date: "",
        description:
          "SalesSpaice is\n\t- a central, digital place helping sales professionals close complex deals faster\n\t- a digital colleague that increases the productivity of sales teams\n\nAlong the entire sales process, SalesSpaice provides sales teams who sell software or other complex products and services â€œSpaicesâ€ in which digital AI agents support and collaborate to get things done.",
        title: "CEO/Founder",
        company: "SalesSpaice",
        company_linkedin: "",
        location: "Bonn, North Rhine-Westphalia, Germany",
      },
      {
        months_duration: "13",
        start_date: "02-2023",
        end_date: "02-2024",
        description:
          "Skills: Hunter Â· Sales Â· Communication Â· Deals Â· Information and Communications Technology (ICT)",
        title: "Regional Sales Director",
        company: "Baxter Planning",
        company_linkedin: "https://www.linkedin.com/company/36982/",
        location: "Bonn, North Rhine-Westphalia, Germany",
      },
      {
        months_duration: "14",
        start_date: "01-2022",
        end_date: "02-2023",
        description:
          "Skills: Hunter Â· Communication Â· Deals Â· Information and Communications Technology (ICT)",
        title: "Senior Account Director Supply Chain Management",
        company: "Coupa Software",
        company_linkedin: "https://www.linkedin.com/company/99595/",
        location: "",
      },
      {
        months_duration: "18",
        start_date: "08-2020",
        end_date: "01-2022",
        description:
          "Skills: Hunter Â· Communication Â· Deals Â· Information and Communications Technology (ICT)",
        title: "Area Sales Director",
        company: "E2open",
        company_linkedin: "https://www.linkedin.com/company/7677/",
        location: "",
      },
      {
        months_duration: "12",
        start_date: "06-2019",
        end_date: "05-2020",
        description:
          "Skills: Hunter Â· Communication Â· Deals Â· Information and Communications Technology (ICT)",
        title: "Senior Account Executive",
        company: "SAS",
        company_linkedin: "https://www.linkedin.com/company/1491/",
        location: "KÃ¶ln und Umgebung, Deutschland",
      },
      {
        months_duration: "49",
        start_date: "05-2015",
        end_date: "05-2019",
        description:
          "Account management of and sales into large aviation and logistics customers.",
        title: "Senior Sales Executive",
        company: "Quintiq, a Dassault SystÃ¨mes company",
        company_linkedin: "https://www.linkedin.com/company/16797/",
        location: "DÃ¼sseldorf Area, Germany",
      },
      {
        months_duration: "46",
        start_date: "07-2011",
        end_date: "04-2015",
        description:
          "â€¢\tSell complex aviation software to airports, airlines, ground handling companies and others\nâ€¢\tGive sales presentations in both English and German\nâ€¢\tGive presentations to large groups at industry conferences\nâ€¢\tBuild relationships at all levels of customers' organizations\nâ€¢\tNegotiate customer contracts from draft to signature\nâ€¢\tAnalyze customer requirements for tender responses\nâ€¢\tRepresent INFORM at trade shows\nâ€¢\tDevelop sales strategies with partner companies for complementary solutions",
        title: "Business Development Manager",
        company: "INFORM GmbH",
        company_linkedin: "",
        location: "Kreisfreie Stadt Aachen Area, Germany",
      },
      {
        months_duration: "13",
        start_date: "06-2010",
        end_date: "06-2011",
        description:
          "â€¢\tSold pilot training services and dry-lease flight simulator capacity \nâ€¢\tCreated concepts for and conducted customer visits in Europe and Africa \nâ€¢\tParticipated in customer contract negotiations \nâ€¢\tCreated and maintained customer contracts \nâ€¢\tPrepared market forecasts \nâ€¢\tRepresented LFT-CST at aviation trade shows \nâ€¢\tImplemented Microsoft Business Contact Manager (CRM solution)",
        title: "Sales Manager",
        company: "Lufthansa Flight Training CST GmbH",
        company_linkedin: "",
        location: "Berlin Area, Germany",
      },
      {
        months_duration: "40",
        start_date: "04-2007",
        end_date: "07-2010",
        description:
          'â€¢\tDeveloped and implemented marketing strategies \nâ€¢\tCreated and presented marketing material concerning operating costs and performance of Embraer aircraft and their competitors to large, medium and small airlines\nâ€¢\tDeveloped of a "Demand Allocation Model" used to predict airline passenger flows. Results of this model were used in presentations to major North American airlines (Tool used: Microsoft Access)\nâ€¢\tCreated ad-hoc analyses for colleagues in Sales and Marketing, including material used by the senior management team in Brazil',
        title: "Airline Marketing Analyst",
        company: "Embraer Aircraft",
        company_linkedin: "https://www.linkedin.com/company/4211/",
        location: "Miami/Fort Lauderdale Area",
      },
      {
        months_duration: "21",
        start_date: "08-2004",
        end_date: "04-2006",
        description:
          "Provided aviation technical information to colleagues with little or no aviation background. Specific activities included:\n\nâ€¢\tExplaining aircraft and airport restrictions and limitations \nâ€¢\tWorking closely with chief pilots of new aircraft to ensure accuracy of technical information provided to prospective customers \nâ€¢\tCreating detailed aircraft performance analyses \nâ€¢\tManaging production of marketing materials by vendors \nâ€¢\tGiving aircraft tours to prospective clients at static displays",
        title: "Technical Marketing",
        company: "NetJets",
        company_linkedin: "https://www.linkedin.com/company/165160/",
        location: "Columbus, Ohio Area",
      },
      {
        months_duration: "17",
        start_date: "04-2003",
        end_date: "08-2004",
        description:
          "â€¢\tPlanned and conducted training sessions about aircraft performance for current employees and new hires \nâ€¢\tCollaborated with external software developer to create range mapping tool \nâ€¢\tReviewed upcoming customer flights for potential problems that could diminish customer experience \nâ€¢\tPerformed safety reviews and approvals of airports for use by NetJets Europe aircraft \nâ€¢\tConducted regular presentations about upcoming critical flights to the management team",
        title: "Quality and Safety Review Department",
        company: "NetJets",
        company_linkedin: "https://www.linkedin.com/company/165160/",
        location: "",
      },
      {
        months_duration: "12",
        start_date: "2003",
        end_date: "2004",
        description:
          "Provided aviation technical information to colleagues with little or no aviation background. Specific activities included:\nâ€¢\tExplaining aircraft and airport restrictions and limitations \nâ€¢\tWorking closely with chief pilots of new aircraft to ensure accuracy of technical information provided to prospective customers \nâ€¢\tCreating detailed aircraft performance analyses \nâ€¢\tManaging production of marketing materials by vendors \nâ€¢\tGiving aircraft tours to prospective clients at static displays",
        title: "Sales Support Analyst",
        company: "NetJets Europe",
        company_linkedin: "https://www.linkedin.com/company/368613/",
        location: "Lisbon Area, Portugal",
      },
      {
        months_duration: "36",
        start_date: "2000",
        end_date: "2003",
        description:
          "Worked as part of a project team to implement the SAP Project Systems (PS) and Controlling (CO) modules.\n\nâ€¢\tAnalyzed client business processes to either adapt the software to match the processes or the processes to match the software \nâ€¢\tCooperated closely with other project teams to coordinate activities and acted as point of contact for changes to SAP PS and CO modules during final system development phase \nâ€¢\tDocumented software transactions",
        title: "Consultant",
        company: "BearingPoint",
        company_linkedin: "https://www.linkedin.com/company/1349/",
        location: "Frankfurt Area, Germany",
      },
      {
        months_duration: "12",
        start_date: "1999",
        end_date: "2000",
        description:
          "Learned client business processes on site in the US and Germany in order to create realistic customized written training materials in English and German for SAP implementations.",
        title: "Consultant",
        company: "DDS (SAP training)",
        company_linkedin: "",
        location: "Greater Minneapolis-St. Paul Area",
      },
    ],
  };
</script>

<div class="p-8">
  <section>
    <div class="w-full sm:py-4 lg:px-6">
      <div class="grid md:grid-cols-12 gap-4 h-full">
        <div
          class="md:col-span-5 bg-white flex flex-col background-white h-[48rem] p-6 rounded-2xl border border-gray-100"
        >
          <div
            class="flex flex-row gap-4 justify-between border-b border-gray-100 pb-6"
          >
            <div class="flex flex-row gap-4">
              <img
                src={retzer.profile_picture}
                alt="user profile"
                class="w-20 rounded-full border border-black border-7 border-opacity-80"
              />
              <div class="flex flex-col">
                <h1 class="text-2xl font-medium leading-tight">Rick Retzer</h1>
                <p class="text-medium text-gray-500 mb-1">
                  SalesSpaice - Close more deals
                </p>
                <div class="flex flex-row gap-1">
                  {#each retzer.languages as language}
                    <Badge class="text-xs">{language.language}</Badge>
                  {/each}
                </div>
              </div>
              <div class="flex flex-row gap-1">
                <EditIcon class="w-4 h-4" />
              </div>
            </div>
            <div class="flex flex-row self-start">
              <Badge
                class="bg-orange-400 hover:bg-orange-600 transition-colors ease-in-out duration-300"
                >Pending</Badge
              >
            </div>
          </div>
          <div class="flex flex-row gap-4 pt-6"></div>
        </div>
        <!-- <div class="md:col-span-4 bg-stone-50">
          <a
            href=""
            class="group relative flex flex-col overflow-hidden rounded-lg px-4 pb-4 pt-40 mb-4"
          >
            <img
              src="https://images.unsplash.com/photo-1504675099198-7023dd85f5a3?q=80&w=2940&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
              alt=""
              class="absolute inset-0 h-full w-full object-cover group-hover:scale-105 transition-transform duration-500 ease-in-out"
            />
            <div
              class="absolute inset-0 bg-gradient-to-b from-gray-900/25 to-gray-900/5"
            ></div>
            <h3
              class="z-10 text-2xl font-medium text-white absolute top-0 left-0 p-4 xs:text-xl md:text-3xl"
            >
              Gin
            </h3>
          </a>
          <div class="grid gap-4 grid-cols-2 sm:grid-cols-4 lg:grid-cols-2">
            <a
              href=""
              class="group relative flex flex-col overflow-hidden rounded-lg px-4 pb-4 pt-40"
            >
              <img
                src="https://images.unsplash.com/photo-1571104508999-893933ded431?q=80&w=2940&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                alt=""
                class="absolute inset-0 h-full w-full object-cover group-hover:scale-105 transition-transform duration-500 ease-in-out"
              />
              <div
                class="absolute inset-0 bg-gradient-to-b from-gray-900/25 to-gray-900/5"
              ></div>
              <h3
                class="z-10 text-2xl font-medium text-white absolute top-0 left-0 p-4 xs:text-xl md:text-3xl"
              >
                Whiskey
              </h3>
            </a>
            <a
              href=""
              class="group relative flex flex-col overflow-hidden rounded-lg px-4 pb-4 pt-40"
            >
              <img
                src="https://images.unsplash.com/photo-1626897505254-e0f811aa9bf7?q=80&w=2940&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                alt=""
                class="absolute inset-0 h-full w-full object-cover group-hover:scale-105 transition-transform duration-500 ease-in-out"
              />
              <div
                class="absolute inset-0 bg-gradient-to-b from-gray-900/25 to-gray-900/5"
              ></div>
              <h3
                class="z-10 text-2xl font-medium text-white absolute top-0 left-0 p-4 xs:text-xl md:text-3xl"
              >
                Vodka
              </h3>
            </a>
          </div>
        </div>
        <div
          class="col-span-2 sm:col-span-1 md:col-span-3 bg-sky-50 h-auto md:h-full flex flex-col"
        >
          <a
            href=""
            class="group relative flex flex-col overflow-hidden rounded-lg px-4 pb-4 pt-40 flex-grow"
          >
            <img
              src="https://images.unsplash.com/photo-1693680501357-a342180f1946?q=80&w=2940&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
              alt=""
              class="absolute inset-0 h-full w-full object-cover group-hover:scale-105 transition-transform duration-500 ease-in-out"
            />
            <div
              class="absolute inset-0 bg-gradient-to-b from-gray-900/25 to-gray-900/5"
            ></div>
            <h3
              class="z-10 text-2xl font-medium text-white absolute top-0 left-0 p-4 xs:text-xl md:text-3xl"
            >
              Brandy
            </h3>
          </a>
        </div>
      </div> -->
      </div>
    </div>
  </section>
</div>
