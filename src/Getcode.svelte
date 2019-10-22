<script>
  import Modal from "./Modal.svelte";

  let showModal = false;
  function alertmenssage() {
    alert("感谢你的申请，我们会尽快给您回复！");
  }
</script>

<style>
  input {
    font-size: 14px;
    margin-right: -4px;
    padding: 0 0.5em 0;
    height: 40px;
    border: 1px solid #7D10F2;
    border-bottom-right-radius: 0;
    border-top-right-radius: 0;
  }
  .getCD {
    font-size: 15px;
    margin: 0 auto;
    padding: .5em 1em;
	background-color: aquamarine;
    border-radius: 8px;
    display: block;
  }
  button {
    border: 0;
  }
  .Midd {
    margin: 0 auto;
    display: inherit;
    margin-bottom: 1em;
  }
</style>

<button class="getCD" on:click={() => (showModal = true)}>
  申请成为代理
</button>

{#if showModal}
  <Modal on:submit={() => (showModal = false)}>
    <input class="Midd" placeholder="输入代理邀请码" />
  </Modal>
{/if}
