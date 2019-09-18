<script>
  import { onMount } from "svelte";
  import Category from "./Category.svelte";

  export let unit = {
    unitname: "Behance",
    imgurl: "",
    linkurl: ""
  };
  let products = [];
  let categories = [];
  let height = "300px";

  async function preload() {
    await fetch("https://api.sheety.co/f2c23106-ef0f-4d73-8a89-b89c9e190cb9")
      .then(function(response) {
        return response.json();
      })
      .then(function(result) {
        products = [...result];
        let tmpCategories = products.map(item => {
          return item.category;
        });
        categories = [...new Set(tmpCategories)];
      });
  }

  onMount(preload);
</script>

<style>
  .box {
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    background-color: #ffbfcb;
    padding: 2em;
    opacity: 0.8;
    color: #000;
    display: block;
  }

</style>

<div class="box">
  <Category {categories} />
  <ul>
    {#each products as item, i}
      <!-- content here -->
      <li>{i} {item.product} ¥{item.price}</li>
    {/each}
  </ul>
</div>
