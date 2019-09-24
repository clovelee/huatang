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
 ul {padding-inline-start:0;}

  .box {
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    background-color: #fff;
    padding: 2em;
    opacity: 0.8;
    color: #000;
    display: block;
  }
	.box li {
		list-style: none;
		line-height: 2em;
	}
	.prt-index {
		font-size: 12px;
		color: #666;
		padding-right:1em;
	}
	.prt-name {
		font-size: 14px;
		font-weight: 500;
		padding-right:1em;
	}
	.prt-price {
		font-size: 14px;
		color: brown;
	}

</style>

<div class="box">
  <Category {categories} />
  <ul>
    {#each products as item, i}
      <!-- content here -->
      <li>
				<span class="prt-index">{i}</span>
				<span class="prt-name">{item.product}</span>
				<span class="prt-price">¥{item.price}</span></li>
    {/each}
  </ul>
</div>
