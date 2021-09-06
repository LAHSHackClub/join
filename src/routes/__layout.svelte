
<main>
	<slot></slot>
</main>

<style global>
	body {
		background: #e0e0e0;
		box-sizing: border-box;
		display: grid;
		place-items: center;

		margin: 0;
		height: 100vh;
		padding: 10px;
		overflow: hidden;

		font-family: "Atkinson Hyperlegible", sans-serif;
	}

	main {
		display: grid;
		place-items: center;
		grid-template-columns: 1fr;
		grid-template-rows: 1fr;

		max-width: 600px;
		width: 100%;
	}

	main > div {
		box-sizing: border-box;
		grid-column: 1 / 1;
		grid-row: 1 / 1;
		width: 100%;
	}
</style>