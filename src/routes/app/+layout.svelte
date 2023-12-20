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
        <button
          type="button"
          class="btn-icon variant-filled-primary w-10 border-2 border-primary-900-50-token"
        >
          <iconify-icon icon="solar:user-bold" width="20" />
        </button>
      </svelte:fragment>
    </AppBar>
  </svelte:fragment>
  <slot />
</AppShell>
