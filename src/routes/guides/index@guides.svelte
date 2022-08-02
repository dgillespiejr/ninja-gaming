<script context="module">
	// This function runs automatically by SvelteKit, and on the server when accessed directly instead of a clicked link
	// @ts-ignore
	export async function load({ fetch }) {
		// const res = await fetch('https://jsonplaceholder.typicode.com/posts');
		const res = await fetch('/guides.json');
		const { guides } = await res.json();
		// console.log(guides);

		if (res.ok) {
			return {
				props: {
					guides
				}
			};
		}
		return {
			status: res.status,
			error: new Error('Could not fetch guides.')
		};
	}
</script>

<script>
	export /**
	 * @type {any}
	 */
	let guides;
</script>

<div class="guides">
	<ul>
		{#each guides as guide (guide.id)}
			<li>
				<a sveltekit:prefetch href={`/guides/${guide.id}`}>{guide.title}</a>
			</li>
		{/each}
	</ul>
</div>

<style>
	.guides {
		margin: 20px auto;
	}

	ul {
		list-style-type: none;
		padding: 0;
	}

	a {
		display: inline-block;
		margin-top: 10px;
		padding: 10px;
		border: 1px dotted rgba(255, 255, 255, 0.2);
	}
</style>
