<script>
	import Project from "./Project.svelte";
	import projecten from './projecten.json'

	let current = 0

	const click = () => {
		if (current === projecten.length - 1) {
			current = 0
		} else {
			current++
		}
	}
</script>

<main>
	<h1>Nierot</h1>
	<h2>ik maak websites ofzo</h2>

	<button on:click={click}>
		<i class="fas fa-arrow-right"></i>
	</button>

	<div id="projecten">
		<Project {...projecten[current]}/>
	</div>

</main>

<style>

	main {
		text-align: center;
		padding: 1em;
		height: 100%;
	}

	h1 {
		font-weight: 100;
	}

	h2 {
		font-weight: 100;
	}

	#projecten {
		padding-top: 20px;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}
</style>