<script>
	// @ts-ignore
	import MyPhoto from '$lib/assets/MyPhoto.jpg?w=350&webp';
</script>

<div class="container md:w-[90%] xl:w-[80%] h-full mx-auto flex max-xl:flex-col-reverse justify-center items-center xl:border-x border-tertiary-700 p-4 bg-surface-800">
	<div class="space-y-5 xl:w-1/2">
		{#each { length: 0 } as hello}
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse minus porro beatae id
				assumenda natus at error nemo veritatis eum sed tempora unde quo repellendus obcaecati
				nobis, fugit harum facere!
			</p>
		{/each}
		<div>
			<h2 class="py-4">
				<span class="text-6xl">
					Olet saapunut Nicon portofilioon!
				</span>
					
				
				
			</h2>
			<p>
				Täällä esittelen mitä koodiprojekteja olen tehnyt, ja kerron vähän itsestäni
			</p>
			<br>
			<p>
				Olen Joensuusta Lappeenrantaan muuttanut yliopisto-opiskelija. Opiskelen tietotekniikkaa Lappeenranta-Lahti Teknillisessä Yliopistossa (LUT). Pidän alaa erittäin kiinnostavana ja toivon saavani tulevaisuudessa työllistyä alalle.
			</p>
		</div>


	</div>
	<div class="m-10 card">
		<!-- svelte-ignore a11y-img-redundant-alt -->
		<img src={MyPhoto} alt="Photo of me" class="p-7 hover:scale-105 ease-in-out duration-100"/>
	</div>

</div>
