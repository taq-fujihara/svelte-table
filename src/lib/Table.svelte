<div class="container" style={containerStyle}>
  <table>
    <TableColGroup {columns} />
    <TableBody {columns} {data} />
    <TableHeader {columns} />
  </table>
</div>

<script>
  import TableColGroup from './TableColGroup.svelte'
  import TableHeader from './TableHeader.svelte'
  import TableBody from './TableBody.svelte'

  export let width = undefined
  export let height = undefined
  export let columns = []
  export let data = []

  $: containerStyle = [
      width !== undefined ? `width: ${width}px` : '',
      height !== undefined ? `height: ${height}px` : '',
    ].join(';')
</script>

<style>
  * {
    box-sizing: border-box;
  }

  .container {
    position: relative;
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
    /* width: 100%; */
    width: 0;
  }
</style>
