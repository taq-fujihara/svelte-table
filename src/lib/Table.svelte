<div class="container">
  <table>
    {#each columns as column}
      <col style={`width: ${column.width}px`}>
    {/each}
    <tbody>
      {#each data as datum}
        <tr>
          {#each columns as column}
            <td class={column.fixed && 'fixed-cell'}>
              {datum[column.name]}
            </td>
          {/each}
        </tr>
      {/each}
    </tbody>
    <thead>
      <tr>
        {#each columns as column, i}
          <th class={column.fixed && 'fixed-cell'}>
            {column.name}
          </th>
        {/each}
      </tr>
    </thead>
  </table>
</div>

<script>
  let columns = [
    {
      name: 'col1',
      width: 150,
      fixed: true,
    },
    {
      name: 'col2',
      width: 150,
    },
    {
      name: 'col3',
      width: 150,
    },
    {
      name: 'col4',
      width: 150,
    },
    {
      name: 'col5',
      width: 150,
    },
  ]
  let data = [
    { col1: 'val1', col2: 'val2', col3: 'val3', col4: 'val4', col5: 'val5' },
    { col1: 'val1', col2: 'val2', col3: 'val3', col4: 'val4', col5: 'val5' },
    { col1: 'val1', col2: 'val2', col3: 'val3', col4: 'val4', col5: 'val5' },
    { col1: 'val1', col2: 'val2', col3: 'val3', col4: 'val4', col5: 'val5' },
    { col1: 'val1', col2: 'val2', col3: 'val3', col4: 'val4', col5: 'val5' },
    { col1: 'val1', col2: 'val2', col3: 'val3', col4: 'val4', col5: 'val5' },
    { col1: 'val1', col2: 'val2', col3: 'val3', col4: 'val4', col5: 'val5' },
  ]
</script>

<style>
  * {
    box-sizing: border-box;
  }

  .container {
    position: relative;
    width: 500px;
    height: 200px;
    overflow: auto;

    border-top: 1px solid #e0e0e0;
    border-bottom: 1px solid #e0e0e0;
    border-left: 1px solid #e0e0e0;
    border-right: 1px solid #e0e0e0;
  }

  table {
    position: relative;
    table-layout: fixed;
    border-collapse: separate;
    border-spacing: 0;
    width: 100%;
  }

  thead {
    position: sticky;
    top: 0;
  }

  th, td {
    padding: 10px;
  }

  th {
    background-color: #eee;
    border-bottom: 1px solid #e0e0e0;
  }
  th:not(:first-child) {
    border-left: 1px solid #e0e0e0;
  }

  td {
    background-color: #fff;
  }
  td:not(:first-child) {
    border-left: 1px solid #e0e0e0;
  }

  tr:not(:last-child) td {
    border-bottom: 1px solid #e0e0e0;
  }

  .fixed-cell {
    position: sticky;
    left: 0;
    border-right: 1px solid #e0e0e0;
  }

  .first-of-non-fixed-cell {
    border-left: 0;
  }
</style>
