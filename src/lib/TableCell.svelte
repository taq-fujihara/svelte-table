<td class={column.fixed && 'fixed-cell'}>
  {data[column.name]}
</td>

<script>
  export let column = {}
  export let data = {}
</script>

<style>
  td {
    padding: 10px;
    background-color: #fff;
    border-bottom: 1px solid #e0e0e0;
  }

  td:not(:first-child) {
    border-left: 1px solid #e0e0e0;
  }

  .fixed-cell {
    position: sticky;
    left: 0;
    border-right: 1px solid #e0e0e0;
  }
</style>
