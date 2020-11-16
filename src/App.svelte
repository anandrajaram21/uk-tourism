<script>
	import TailwindCss from './TailwindCss.svelte';
	import { onMount } from 'svelte';
	import Typed from 'typed.js';
	var options = {
		strings: ['hello', 'goodbye'],
		typeSpeed: 40,
		loop: true
	}
	onMount(() => {
		var typed  = new Typed('.typing', options);
	})
	export let name;
</script>
<TailwindCss/>

<body>
	<h1 class="bg-blue-900 text-white p-5">Hello {name}!</h1>
	<div class="bg-red-500 p-5 text-white">
		<p class="typing inline"></p>
	</div>
</body>