<script lang="ts">
	// The ordering of these imports is critical to your app working properly
	import '@skeletonlabs/skeleton/themes/theme-crimson.css';
	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import '@skeletonlabs/skeleton/styles/all.css';
	// Most of your app wide CSS should be put in this file
	import '../app.postcss';
	import { AppShell, AppBar, Drawer, drawerStore } from '@skeletonlabs/skeleton';
	import type { DrawerSettings } from '@skeletonlabs/skeleton';
	import NavI from '$lib/navI.svelte';
	import hamburger from '$lib/hamburger.svelte';
	import Hamburger from '$lib/hamburger.svelte';

	function onClick() {
		drawerStore.open();
		console.log('Hello world');
	}
</script>

<Drawer>
	<NavI />
</Drawer>

<AppShell>
	<svele:fragment slot="header">
		<AppBar>
			<svelte:fragment slot="lead">
				<h1 class="p-2">Nicon portfolio</h1>
			</svelte:fragment>

			<svelte:fragment slot="trail">
				<NavI isRow={true} />

				<button on:click={onClick}>
					<div class="sm:hidden">
						<Hamburger />
					</div>
				</button>
			</svelte:fragment>
		</AppBar>
	</svele:fragment>
	<svelte:fragment>
		<div
			class="container mx-auto flex h-full items-center justify-center border-tertiary-700 bg-surface-700 p-4 max-xl:flex-col-reverse md:w-[90%] xl:min-w-[80%] xl:border-x"
		>
			<slot />
		</div>
	</svelte:fragment>
</AppShell>
