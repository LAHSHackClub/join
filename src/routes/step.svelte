
<script lang="ts">
	import { fade } from "svelte/transition";
	import { onMount } from "svelte";

	let query = 0;
	let short = "";
	onMount(() => {
		query = parseInt(new URLSearchParams(window.location.search).get("query"));
		short = opts[query].replace("https://", "").substring(0, 15) + "...";
	});

	const opts = [
		"https://docs.google.com/forms/d/e/1FAIpQLSf9RoZ_nRE6y5beHrqFoW-TTHIpETOt_DubVGAkk4g4j8xX7A/viewform"
	]
</script>

<svelte:head>
	<title>LAHS Hack Club - Join Step</title>
</svelte:head>
<div transition:fade="{{duration:100}}">
	<p><a href="/" class="btn">← Done? Go back</a></p>
	<a href="{opts[query]}" target="_blank">(not working? open {short} in a new tab)</a>
	<br>
	<iframe title="Action Window" src="{opts[query]}"></iframe>
</div>

<style>
	div {
		border-radius: 20px;
		background: #e0e0e0;
		box-shadow:  20px 20px 60px #bebebe,
								-20px -20px 60px #ffffff;
		padding: 20px;

		display: flex;
		flex-direction: column;
		min-height: 85vh;
	}

	@media (min-height: 992px) {
		div {
			min-height: 70vh;
		}
	}

	p {
		margin-top: 0;
	}

	a {
		color: #0079F4;
		text-decoration: none;
	}

	.btn {
		color: #eee;

		border-radius: 10px;
		background: #002333;
		box-shadow: inset 6px 6px 12px #000e14,
								inset -6px -6px 12px #003852;

		display: block;
		padding: 15px 20px;
	}

	iframe {
		border-radius: 10px;
		flex: 1 1;
	}
</style>
