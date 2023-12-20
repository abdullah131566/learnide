<script>
  import { AppShell, AppBar, Avatar } from '@skeletonlabs/skeleton';
  import LearnideLogo from '../../../assets/learnide-logo.svg';
  import LearnideTitle from '../../../assets/learnide-title.svg';
  import LearnideTitleLight from '../../../assets/learnide-title-light.svg';

  const emailInitials = 'AB';
  let isDarkMode = true;

  $: titleImage = isDarkMode ? LearnideTitleLight : LearnideTitle;
</script>

<AppShell>
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
