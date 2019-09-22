<script>
	import Modal from './Modal.svelte';

	let showModal = false;
	function alertmenssage() {
		alert("感谢你的申请，我们会尽快给您回复！")
	}
</script>
<style>
  .btn {
    font-size: 14px;
    background-color: blueviolet;
    color: #fff;
    padding: 0 0.5em 0;
    border-bottom-left-radius: 0;
    border-top-left-radius: 0;
    height: 40px;
    border: 1px solid blueviolet;
  }
  input {
    font-size: 14px;
    margin-right: -4px;
    padding: 0 0.5em 0;
    height: 40px;
    border: 1px solid blueviolet;
    border-bottom-right-radius: 0;
    border-top-right-radius: 0;
  }
	.getCD {
		font-size:14px;
		margin-top: 1em;
		padding: 2px 4px;
		color: #fff;
		font-weight: 500;
		background-color: rgba(247, 90, 173, 0.856);
		border-radius: 4px;
		display: inline-block;
	}
	button {
		border: 0;
	}
	.Midd {margin: 0 auto;display: inherit;margin-bottom: 1em;}
</style>

<form action="/" method="POST" data-netlify="true" >
	<input name="phone" placeholder="输入电话号码" />
	<button class="btn" on:click={alertmenssage}>获取代理邀请</button>
</form>

<button class="getCD" type="submit" on:click="{() => showModal = true}">点击查看代理价</button>

{#if showModal}
	<Modal on:submit="{() => showModal = false}">
		<input class="Midd" placeholder="输入代理邀请码" />
	</Modal>
{/if}
