<script>
  export let categories = [];
</script>

<style>
ul {padding-inline-start:0;}
ul li {list-style: none;font-size: 12px;display: inline-block;padding-right: 4px;}
button {border-radius: 20%;}
</style>

<div class="box">
  <h4>选择产品类别</h4>
  <ul>
    {#each categories as item, i}
      <!-- content here -->
      <li>
        <button>{item}</button>
      </li>
    {/each}
  </ul>
</div>
