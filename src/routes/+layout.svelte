<script lang="ts">
	// The ordering of these imports is critical to your app working properly
	import '@skeletonlabs/skeleton/themes/theme-crimson.css';
	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import '@skeletonlabs/skeleton/styles/all.css';
	// Most of your app wide CSS should be put in this file
	import '../app.postcss';
	import { AppShell, AppBar } from '@skeletonlabs/skeleton';
	import NavI from '$lib/navI.svelte';
</script>

<AppShell>
	<svele:fragment slot="header">
		<AppBar>
			<svelte:fragment slot="lead">
				<h1 class="p-2">Nicon portfolio</h1>
			</svelte:fragment>

			<svelte:fragment slot="trail">
				<NavI isRow={true} />
			</svelte:fragment>
		</AppBar>
	</svele:fragment>
	<svelte:fragment>
		<slot />
	</svelte:fragment>
</AppShell>
