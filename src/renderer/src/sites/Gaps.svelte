<script lang="ts">
  import gapsData from '../config.json'
  import { path } from '../stores/stores.js'

  let currentPath

  path.subscribe((value) => {
    currentPath = value
  })
</script>

{#if gapsData}
  <div>
    <p>Inner Gap Value: {gapsData.gaps.inner.command}</p>
    <p>Outer Gap Value: {gapsData.gaps.outer.command}</p>
  </div>
{/if}
<div>
  {currentPath}
</div>
