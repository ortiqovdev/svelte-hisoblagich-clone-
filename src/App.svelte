<script lang="ts">
	let count :number = 0
	function onMinus(){
		count = count - 1
	}
	function onPlus(){
		count = count + 1
	}
	function onZero(){
		count = 0
	}


</script>
<h3 id="counter">{count}</h3>
<div class="buttons">
	<button on:click={onMinus} id="minus">-</button>
	<button on:click={onZero} id="zero">0</button>
	<button on:click={onPlus} id="plus">+</button>
</div>
<style>
	#counter {
		font-size: 120px;
	}
	.buttons {
		display: flex;
		gap: 15px;
	}
	button {
		color: white;
		width: 100px;
		height: 45px;
		background-color: black;
		border: none;
		border-radius: 20px;
		font-size: 28px;
	}
	button:hover {
		background-color: rgb(74, 74, 74);
		transition: 1s all ease;
		transform: translateY(-5px);
		color: red;
		font-size: 30px;
	}
</style>
