<tr>
  {#each columns as column}
    <TableCell {column} {data} />
  {/each}
</tr>

<script>
  import TableCell from './TableCell.svelte'

  export let columns = []
  export let data = {}
</script>
