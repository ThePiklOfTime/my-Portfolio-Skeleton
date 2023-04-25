<script lang="ts">
	export let isRow = false;
	let navClass = 'list-nav';
	let liClass = 'gap-10';
	import { page } from '$app/stores';
	if (isRow) {
		navClass = 'list-nav max-sm:hidden';
		liClass = 'flex flex-row gap-10';
	}
	$: Active = (href: string) => (href === $page.url.pathname ? '!bg-primary-500' : '');
</script>

<nav class={navClass}>
	<!-- (optionally you can provde a label here) -->
	<ul>
		<li class={liClass}>
			<span>
				<a href="/" class={Active('/')}>
					<span>Home</span>
				</a>
			</span>
			<span>
				<a href="/about" class={Active('/about')}>
					<span>About</span>
				</a>
			</span>
		</li>
	</ul>
</nav>
