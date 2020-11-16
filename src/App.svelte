<script>
	import TailwindCss from './TailwindCss.svelte';
	export let name;
</script>
<TailwindCss/>

<main>
	<h1 class="bg-blue-500">Hello {name}!</h1>
</main>