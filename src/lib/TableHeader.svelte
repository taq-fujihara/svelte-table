<thead>
  <tr>
    {#each columns as column}
      <TableHeaderCell {column} />
    {/each}
  </tr>
</thead>

<script>
  import TableHeaderCell from './TableHeaderCell.svelte'

  export let columns = []
</script>

<style>
  thead {
    position: sticky;
    top: 0;
  }
</style>
