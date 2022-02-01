<main>
  <div>
    <button on:click={setSize}>Set Size</button>
    <button on:click={clearSize}>Clear Size</button>
  </div>

  <Table width={width} height={height} {columns} {data} />
</main>

<script>
  import Table from './lib/Table.svelte'

  const columns = [
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

  const data = [
    { col1: 'val1', col2: 'val2', col3: 'val3', col4: 'val4', col5: 'val5' },
    { col1: 'val1', col2: 'val2', col3: 'val3', col4: 'val4', col5: 'val5' },
    { col1: 'val1', col2: 'val2', col3: 'val3', col4: 'val4', col5: 'val5' },
    { col1: 'val1', col2: 'val2', col3: 'val3', col4: 'val4', col5: 'val5' },
    { col1: 'val1', col2: 'val2', col3: 'val3', col4: 'val4', col5: 'val5' },
    { col1: 'val1', col2: 'val2', col3: 'val3', col4: 'val4', col5: 'val5' },
    { col1: 'val1', col2: 'val2', col3: 'val3', col4: 'val4', col5: 'val5' },
  ]

  let width = undefined
  let height = undefined

  const setSize = () => {
    width = 500
    height = 200
  }

  const clearSize = () => {
    width = undefined
    height = undefined
  }
</script>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
      Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }
</style>
