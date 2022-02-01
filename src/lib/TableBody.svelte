<tbody>
  {#each data as datum}
    <TableRow {columns} data={datum} />
  {/each}
</tbody>

<script>
  import TableRow from './TableRow.svelte'

  export let columns = []
  export let data = []
</script>
