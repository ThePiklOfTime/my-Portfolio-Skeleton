<script lang="ts">
	// @ts-ignore
	import MyPhoto from '$lib/assets/MyPhoto.jpg?width=500&format=webp';
	let witdh:number = 0;
	

	
</script>

<svelte:window bind:innerWidth={witdh}></svelte:window>

<div class="space-y-5 xl:w-1/2">
	{#each { length: 0 } as hello}
		<p>
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse minus porro beatae id assumenda
			natus at error nemo veritatis eum sed tempora unde quo repellendus obcaecati nobis, fugit
			harum facere!
		</p>
	{/each}
	<div>
		<h2 class="py-4">
			<span class="text-6xl"> Olet saapunut Nicon portofilioon!</span>
		</h2>
		<p>Täällä esittelen mitä koodiprojekteja olen tehnyt, ja kerron vähän itsestäni</p>
		<br />
		<p>
			Olen Joensuusta Lappeenrantaan muuttanut yliopisto-opiskelija. Opiskelen tietotekniikkaa
			Lappeenranta-Lahti Teknillisessä Yliopistossa (LUT). Pidän alaa erittäin kiinnostavana ja
			toivon saavani tulevaisuudessa työllistyä alalle.
		</p>
	</div>
</div>
<div class="card m-10 xl:max-w-[30%]">
	<img src={MyPhoto} alt="Nico's portrait" class="p-7 duration-100 ease-in-out hover:scale-105" />
</div>
