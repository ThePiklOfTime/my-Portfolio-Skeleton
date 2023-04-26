<script lang="ts">
	export let isRow = false;
	let navClass = 'list-nav';
	let liClass = 'gap-10';
	import { page } from '$app/stores';
	import { drawerStore } from '@skeletonlabs/skeleton';
	if (isRow) {
		navClass = 'list-nav max-sm:hidden';
		liClass = 'flex flex-row gap-10';
	}
	$: Active = (href: string) => (href === $page.url.pathname ? '!bg-primary-500' : '');
	$: {
		console.log($page.url.pathname)
	}
	function onClick(){
		drawerStore.close()
	}
	console.log("Hello world")
</script>

<nav class={navClass}>
	<!-- (optionally you can provde a label here) -->
	<ul>
		<li class={liClass}>
			{#if !isRow}
			<div class="hidden">
				<a href="/" class={Active('/')} on:click={onClick}>
					<span>Home</span>
				</a>
			</div>
			{/if}
			<div class="mx-4 my-6">
				<a href="/" class={Active('/')} on:click={onClick}>
					<span>Home</span>
				</a>
			</div>
			<div class="mx-4 my-6">
				<a href="/about" class={Active('/about')} on:click={onClick}>
					<span>About</span>
				</a>
			</div>
		</li>
	</ul>
</nav>
