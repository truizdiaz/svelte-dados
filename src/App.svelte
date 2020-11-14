<script>
	let dadoIzquierda = "assets/img/dice1.png";
	let dadoDerecha = "assets/img/dice2.png";
	let numero1 = 1;
	let numero2 = 2;

	function tirarDados() {
		numero1 = Math.floor(Math.random() * 6) + 1;
		numero2 = Math.floor(Math.random() * 6) + 1;
		dadoIzquierda = "assets/img/dice" + numero1 + ".png";
		dadoDerecha = "assets/img/dice" + numero2 + ".png";
	}
</script>

<style>
	.img {
		width: 300px;
		height: 300px;
		background-color: red;
		margin: 30px;
		border-radius: 20px;
	}

	.dado {
		height: 100vh;
		background-color: #e9ecef;
	}
</style>

<main class="dado">
	<div class="jumbotron text-center">
		<button class="btn btn-success lg" on:click={tirarDados}>Tirar Dados</button>
		<br />
		<img src={dadoIzquierda} alt="Dado 1" class="img" />
		<img src={dadoDerecha} alt="Dado 2" class="img" />
		{#if numero1 == numero2}
		<h1><span class="badge badge-success"> GANASTE </span></h1>
		{/if}
	</div>
</main>
