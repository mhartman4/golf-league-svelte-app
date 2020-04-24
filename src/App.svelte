<svelte:head>
	<link href="https://fonts.googleapis.com/css?family=Fjalla+One&display=swap" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css?family=Roboto&display=swap" rel="stylesheet">
	<script src="https://code.jquery.com/jquery-3.4.1.min.js"
  integrity="sha256-CSXorXvZcTkaix6Yvo6HppcZGetbYMGWSFlBw8HfCJo="
  crossorigin="anonymous"></script>
	<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">
	  <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js" integrity="sha384-Tc5IQib027qvyjSMfHjOMaLkfuWVxZxUPnCJA7l2mCWNIpG9mGCD8wGNIcPD7Txa" crossorigin="anonymous"></script>
</svelte:head>


<script>
  import Picker from "./Picker.svelte";
	import Weekly from "./Weekly.svelte"
	import Overall from "./Overall.svelte"
  let pages = ["Weekly","Overall"];
	let currentPage = "Weekly";
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
