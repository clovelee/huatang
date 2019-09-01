<script>
  export let categories = [];
</script>

<div class="box">
  <h3>选择产品类别</h3>
  <ul>
    {#each categories as item, i}
      <!-- content here -->
      <li>
        <button>{item}</button>
      </li>
    {/each}
  </ul>
</div>
