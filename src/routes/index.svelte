<script>
	let title = 'Ninja Gaming Guides';

	const updateTitle = () => {
		title = 'Something Completely Different';
	};
</script>

<div class="index">
	<h2>Welcome</h2>
	<p>
		Lorem ipsum dolor sit amet consectetur, adipisicing elit. Officiis, quia et molestiae assumenda
		facilis minima temporibus voluptatum, voluptatibus doloribus, aspernatur provident quod?
		Officiis adipisci consequuntur voluptatibus amet incidunt numquam vero? Ipsam aut molestiae
		itaque voluptates dolore, eaque rerum iste laborum nulla harum natus, officia voluptatibus
		repellendus sint facere saepe delectus possimus, maxime tenetur. Adipisci ipsum quaerat
		perferendis non, ipsam repellendus!
	</p>

	<a href="/guides">View Guides</a>
	<a href="/about">About</a>

	<!-- <button on:click={updateTitle}>Change Title</button>
	<input type="text" bind:value={title} /> -->
</div>

<style>
	.index {
		text-align: center;
		display: block;
		margin: 20px auto;
	}
</style>
