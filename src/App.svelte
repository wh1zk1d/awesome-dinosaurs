<script>
	const name = 'awesome dinosaurs 🦕'
	const img = 'dinosaur.jpg'

	let count = 0

	function addOne() {
		count += 1
	}
</script>

<main>
	<div class="card">
		<h1 class="card--title">Welcome to {name.toUpperCase()}</h1>
		<img src={img} alt="An awesome dinosaur">

		<h2 class="dinosaur-counter">
			{#if count === 0}
				I don't know any cool dinosaurs 😭
			{:else}
				I know {count} pretty nice {count > 1 ? 'dinosaurs' : 'dinosaur'} 🦖
			{/if}
		</h2>
		<button on:click={addOne}>Add a funky dinosaur!</button>
	</div>
</main>

<style>
	.card {
		border: 2px solid #ffc600;
		border-radius: 8px;
		padding: 4rem;
		text-align: center;
	}

	.card--title {
		margin-bottom: 2rem;
	}

	.dinosaur-counter {
		margin-top: 2rem;
		margin-bottom: 1rem;
	}
</style>