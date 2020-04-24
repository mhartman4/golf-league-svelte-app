<script>
 	import Picker from "./Picker.svelte"
	import Weekly from "./Weekly.svelte"
	import Overall from "./Overall.svelte"
  	let pages = ["Weekly","Overall"]
	let currentPage = "Weekly"
</script>

<div id="main">
	<Picker bind:activePage={currentPage} pages={pages} />
	<br><br>
	{#if currentPage === "Weekly"}
		<Weekly></Weekly>
	{:else if currentPage === "Overall"}
		<Overall></Overall>
	{/if}	
</div>	

<style>
	#main {
		max-width: 800px;
		margin: 0 auto;
	}
</style>