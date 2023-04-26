<script>
	import MyPhoto from '$lib/assets/MyPhoto.jpg';
</script>

<div class="container md:w-[90%] xl:w-[80%] h-full mx-auto flex justify-center items-center xl:border-x p-4">
	<div class="space-y-5">
		{#each { length: 10 } as hello}
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse minus porro beatae id
				assumenda natus at error nemo veritatis eum sed tempora unde quo repellendus obcaecati
				nobis, fugit harum facere!
			</p>
		{/each}
		<!-- svelte-ignore a11y-img-redundant-alt -->
		<img src={MyPhoto} alt="Photo of me"/>

	</div>
</div>
