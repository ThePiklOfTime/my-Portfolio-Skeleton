<script>
	// @ts-ignore
	import MyPhoto from '$lib/assets/MyPhoto.jpg?w=350&webp';
</script>

<div class="container md:w-[90%] xl:w-[80%] h-full mx-auto flex max-xl:flex-col-reverse justify-center items-center xl:border-x p-4">
	<div class="space-y-5 xl:w-1/2">
		{#each { length: 5 } as hello}
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse minus porro beatae id
				assumenda natus at error nemo veritatis eum sed tempora unde quo repellendus obcaecati
				nobis, fugit harum facere!
			</p>
		{/each}


	</div>
	<div class="m-10 border-8 border-slate-500 rounded-xl">
		<!-- svelte-ignore a11y-img-redundant-alt -->
		<img src={MyPhoto} alt="Photo of me"/>
	</div>

</div>
