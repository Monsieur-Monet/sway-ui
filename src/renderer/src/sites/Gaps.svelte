<script lang="ts">
  import gapsData from '../config.json'
  
</script>

{#if gapsData}
  <div>
    <p>Inner Gap Value: {gapsData.gaps.inner.command}</p>
    <p>Outer Gap Value: {gapsData.gaps.outer.command}</p>
    <p>{configPath}</p>
  </div>
{/if}
