<script>
  import NavigationButton from './NavigationButton.svelte'
</script>

<div class="flex h-16 bg-slate-500">
  <div class="container m-auto">
    <div class="flex items-center gap-8">
      <NavigationButton href="/" text="Home" />
      <NavigationButton href="/shortcuts" text="Keyboard Shortcuts" />
      <NavigationButton href="/settings" text="Settings" />
    </div>
  </div>
</div>
