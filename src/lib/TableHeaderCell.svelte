<th class={column.fixed && 'fixed-cell'}>
  {column.name}
</th>

<script>
  export let column = {}
</script>

<style>
  th {
    padding: 10px;
    background-color: #eee;
    border-bottom: 1px solid #e0e0e0;
  }

  th:not(:first-child) {
    border-left: 1px solid #e0e0e0;
  }

  .fixed-cell {
    position: sticky;
    left: 0;
    border-right: 1px solid #e0e0e0;
  }
</style>
