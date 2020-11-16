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
	<!-- 
		4 sections in the app
			1. Header section with the navbar and cool typing animation
			2. Places to visit
			3. Uttarakhand Map with leaflet
			4. FAQ sections
			5. Footer that just says made with love by Anand and all that shit
	 -->
	 <header>
		<!-- Navbar -->
		<!-- "Hero" component -->
	</header>
	<section>
		<!-- 
			Places to visit: refer this website https://blog.thomascook.in/10-most-beautiful-places-to-visit-in-uttarakhand/
			Have 5 places of interest
			For each place of interest, there should be 4 points:
				1. Must Visit: 
				2. Things to do:
				3. Best time to visit
				4. A nice looking photo
		-->
	</section>
	<section>
		<!-- 
			Leaflet map with markers at the 5 POIs mentioned in the previous section
		 -->
	</section>
	<section>
		<!-- 
			Put in the FAQs that were there on that thomascook website here, in expandable stuff
		 -->
	</section>
	<footer>
		<!-- 
			The footer, doi
		 -->
	</footer>
	<h1 class="bg-blue-900 text-white p-5">Hello {name}!</h1>
	<div class="bg-red-500 p-5 text-white">
		<p class="typing inline"></p>
	</div>
</body>