
<script lang="ts">
	import { fade } from "svelte/transition";

	const query = [
		"https://docs.google.com/forms/d/e/1FAIpQLSf9RoZ_nRE6y5beHrqFoW-TTHIpETOt_DubVGAkk4g4j8xX7A/viewform"
	]
</script>
<svelte:head>
	<title>Join LAHS Hack Club!</title>
</svelte:head>
<div transition:fade="{{duration:100}}">
	<h1>Join LAHS Hack Club!</h1>
	<p>Just two easy steps:</p>
	<p><a sveltekit:prefetch href="/step?query=0">1. Fill Out The Form</a></p>
	<p><a href="https://lahshackclub.slack.com/join/shared_invite/zt-9nz0ghg0-2HA~bRF4t7MwEPvLaTJlOQ#/shared-invite/email" target="_blank">2. Join Our Slack</a></p>
	<br>
	<p>After that, you're set! Our first meeting is <b>Wensday, September 21st</b> in <b>Room 723.</b> See you there!</p>
</div>
 
<style>
	div {
		border-radius: 10px;
		background: #e0e0e0;
		box-shadow:  20px 20px 60px #bebebe,
								-20px -20px 60px #ffffff;
		padding: 20px;
		transition-duration: 0.5s;
	}

	h1 {
		margin-top: 0;
	}

	p {
		font-size: 1.2rem;
	}

	a {
		color: #eee;
		text-decoration: none;
		
		border-radius: 10px;
		background: #002333;
		box-shadow: inset 6px 6px 12px #000e14,
								inset -6px -6px 12px #003852;

		display: block;
		padding: 15px 20px;
		transition-duration: 0.5s;
	}

	@media (min-width: 512px) {
		div {
			border-radius: 20px;
			padding: 60px;
		}
		a {
			border-radius: 10px;
		}
	}
</style>
