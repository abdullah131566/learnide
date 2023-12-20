<script>
  import { AppShell, AppRail, AppRailAnchor, AppRailTile } from '@skeletonlabs/skeleton';
  import LearnideTitle from '../../../assets/learnide-title.svg';
  import LearnideTitleLight from '../../../assets/learnide-title-light.svg';
  import 'iconify-icon';

  const emailInitials = 'AB';
  let isDarkMode = true;
  let currentTile = 0;

  $: titleImage = isDarkMode ? LearnideTitleLight : LearnideTitle;
</script>

<AppShell>
  <svelte:fragment slot="sidebarLeft">
    <AppRail width="w-20" aspectRatio="aspect-square">
      <svelte:fragment slot="lead">
        <AppRailAnchor href="/app/learnide" target="_blank">
          <svelte:fragment slot="lead"
            ><iconify-icon icon="ph:rocket-launch" width="30" /></svelte:fragment
          >
          <span>App</span>
        </AppRailAnchor>
      </svelte:fragment>
      <!-- --- -->
      <AppRailTile bind:group={currentTile} name="my-flows" value={0} title="my-flows">
        <svelte:fragment slot="lead"
          ><iconify-icon icon="fluent:flow-24-regular" width="30" /></svelte:fragment
        >
        <span>My Flows</span>
      </AppRailTile>
      <AppRailTile bind:group={currentTile} name="community" value={1} title="community">
        <svelte:fragment slot="lead"
          ><iconify-icon icon="gg:community" width="30" /></svelte:fragment
        >
        <span>Community</span>
      </AppRailTile>
      <AppRailTile bind:group={currentTile} name="creator" value={2} title="creator">
        <svelte:fragment slot="lead"
          ><iconify-icon icon="typcn:flow-merge" width="30" /></svelte:fragment
        >
        <span>Creator</span>
      </AppRailTile>
      <!-- --- -->
      <svelte:fragment slot="trail">
        <AppRailAnchor href="/" title="Account">
          <svelte:fragment slot="lead"
            ><iconify-icon
              icon="mingcute:exit-fill"
              width="30"
              flip="horizontal"
            /></svelte:fragment
          >
          <span>Home</span></AppRailAnchor
        >
      </svelte:fragment>
    </AppRail>
  </svelte:fragment>
  <!-- Router Slot -->
  <slot />
  <!-- ---- / ---- -->
</AppShell>
