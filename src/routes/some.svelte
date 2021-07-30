<script>
  import { fade } from "svelte/transition";
  import { onMount } from "svelte";

  let mounted;
  onMount(() => {
    mounted = true;
  });
</script>

<input type="checkbox" bind:checked={mounted} />
{#if mounted}
  <div in:fade|local={{ duration: 1000, delay: 1000 }}>
    <h2>maybe nesting will help?</h2>
  </div>
  <h1 in:fade|local={{ duration: 1000, delay: 2000 }}>headers</h1>
  <h3 in:fade|local={{ duration: 1000, delay: 2250 }}>all of them</h3>
  <input in:fade|local={{ duration: 1000, delay: 2500 }} />
  <div in:fade|local={{ duration: 1000, delay: 2750 }}>plain div</div>
{/if}
