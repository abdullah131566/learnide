<script>
  import { AppShell, AppBar, Avatar } from '@skeletonlabs/skeleton';
  import LearnideLogo from '../../assets/learnide-logo.svg';
  import LearnideTitle from '../../assets/learnide-title.svg';
  import LearnideTitleLight from '../../assets/learnide-title-light.svg';

  const emailInitials = 'AB';
  let isDarkMode = true;

  $: titleImage = isDarkMode ? LearnideTitleLight : LearnideTitle;
</script>

<AppShell>
  <svelte:fragment slot="header">
    <AppBar
      background="bg-surface-50-900-token"
      padding="px-4 py-2"
      border="border-b-2 border-surface-300-600-token"
    >
      <svelte:fragment slot="lead">
        <div class="h-5/6 flex items-center gap-2">
          <img src={LearnideLogo} class="h-6" alt="The Learnide Logo" />
          <img src={titleImage} class="h-4" alt="The Learnide Title" /></div
        >
      </svelte:fragment>
      <svelte:fragment slot="trail">
        <Avatar
          initials={emailInitials}
          width="w-10"
          cursor="cursor-pointer"
          shadow="hover:shadow-md"
          fill="fill-primary-900"
          border="transition duration-500 border-2 border-primary-700-200-token hover:border-primary-600-300-token"
          background="bg-primary-400-500-token"
        />
      </svelte:fragment>
    </AppBar>
  </svelte:fragment>
  <svelte:fragment slot="sidebarLeft">
    <aside class="border-r-2 border-surface-300-600-token px-4 h-full w-80"
      >Sidebar Left alkw rweol rhwoe htrow rhow hoewr htow h Lorem ipsum dolor sit amet consectetur
      adipisicing elit. Harum, fugiat.t</aside
    >
  </svelte:fragment>
  <!-- (sidebarRight) -->
  <svelte:fragment slot="pageHeader">
    <header class="border-b-2 border-surface-300-600-token">Page Header</header>
  </svelte:fragment>
  <!-- Router Slot -->
  <slot />
  <!-- ---- / ---- -->
  <svelte:fragment slot="pageFooter">
    <footer class="border-t-2 border-surface-300-600-token">Page Footer</footer>
  </svelte:fragment>
  <!-- (footer) -->
</AppShell>
