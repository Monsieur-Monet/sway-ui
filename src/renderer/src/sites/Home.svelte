<script lang="ts">
  import { path } from '../stores/stores.js'

  function updatePath(file: File) {
    path.update(() => file.path)
    console.log(file.path)
  }

  function handleFileChange(event: Event) {
    const input = event.target as HTMLInputElement
    const file = input.files[0]
    if (file) {
      updatePath(file)
    }
  }
</script>

<div>
  <h1 class="text-4xl font-bold">Welcome to the Home Page</h1>
  <input type="file" on:change={handleFileChange} />
</div>
