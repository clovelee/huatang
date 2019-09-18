<script>
  import { createEventDispatcher } from "svelte";

  const dispatch = createEventDispatcher();
</script>

<style>
  .modal-background {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.3);
  }
  .modal {
    position: absolute;
    left: 50%;
    top: 50%;
    width: calc(100vw - 5em);
    max-width: 32em;
    max-height: calc(100vh - 5em);
    overflow: auto;
    transform: translate(-50%, -50%);
    padding: 1.5em;
    border-radius: 0.2em;
    background: white;
  }

  button {
    display: block;
    background-color: rgba(247, 90, 173, 0.856);
    border-radius: 4px;
    border: 0;
    width: 100px;
    font-size: 14px;
    list-style: 1.5em;
    margin: 0 auto;
    color: #fff;
    font-weight: 500;
  }
</style>

<div class="modal-background" on:click={() => dispatch('submit')} />

<div class="modal">

  <h4>》加入花糖，查看美妆代理价</h4>
  <slot />
  <button class="btn" on:click={() => dispatch('submit')}>确定</button>
</div>
