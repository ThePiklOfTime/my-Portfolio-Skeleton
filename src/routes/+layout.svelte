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
	import Hamburger from '$lib/hamburger.svelte';

	function onClick() {
		drawerStore.open();
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
			class="container mx-auto flex h-full items-center justify-center bg-surface-700 max-lg:flex-col-reverse sm:border-x sm:border-secondary-500 md:w-[90%] lg:min-w-[80%]"
		>
			<slot />
		</div>
	</svelte:fragment>
	<svelte:fragment slot="footer">
		<footer class="container bg-surface-900 md:w-[90%] lg:min-w-[80%] mx-auto sm:border-x sm:border-secondary-500">
			<div class="">
				<div class="flex flex-col gap-2 card-footer w-[50%] mx-auto p-4 text-center">
					<span> puhelin: +358453171971 </span>
					<span>github: <a href="https://github.com/ThePiklOfTime/">github</a></span>
					<span>sähköposti: nicotolvanen@gmail.com</span>
				</div>
			</div>
		</footer>
	</svelte:fragment>
</AppShell>
