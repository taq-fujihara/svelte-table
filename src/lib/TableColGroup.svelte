{#each columns as column}
  <col style={`width: ${column.width}px`}>
{/each}

<script>
  export let columns = []
</script>
