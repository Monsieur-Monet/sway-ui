<script lang="ts">
  import Navigation from './components/Navigation/Navigation.svelte'
  import Home from './sites/Home.svelte'
  import Shortcuts from './sites/Shortcuts.svelte'
  import Settings from './sites/Settings.svelte'
  import Gaps from './sites/Gaps.svelte'
  let currentPath = window.location.pathname
  let configPath = '/home/timo/.config/sway/config'
</script>

<Navigation />
<div class="container mx-auto mt-4">
  {#if currentPath === '/'}
    <Home />
  {:else if currentPath === '/shortcuts'}
    <Shortcuts />
  {:else if currentPath === '/settings'}
    <Settings />
  {:else if currentPath === '/gaps'}
    <Gaps />
  {:else}
    <div class="text-center mt-8">
      <h1 class="text-4xl font-bold">404</h1>
      <p class="text-xl">Page not found</p>
    </div>
  {/if}
</div>
