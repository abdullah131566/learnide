<script>
  import '../global.css';
  import { AppShell } from '@skeletonlabs/skeleton';
</script>

<AppShell>
  <svelte:fragment slot="header">
    <header class="border border-red-400">Header</header>
  </svelte:fragment>
  <svelte:fragment slot="sidebarLeft">
    <aside class="border border-blue-400 w-full h-full">Sidebar Left</aside>
  </svelte:fragment>
  <!-- (sidebarRight) -->
  <svelte:fragment slot="pageHeader">
    <header class="border border-purple-400">Page Header</header>
  </svelte:fragment>
  <!-- Router Slot -->
  <slot>
    <main class="border border-yellow-400 w-full h-full">Page Content</main>
  </slot>
  <!-- ---- / ---- -->
  <svelte:fragment slot="pageFooter">
    <footer class="border border-green-400">Page Footer</footer>
  </svelte:fragment>
  <!-- (footer) -->
</AppShell>
