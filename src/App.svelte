<script>
	import { onMount } from 'svelte';
	import Icon from './Icon.svelte';
	import Typed from 'typed.js';
	import TailwindCss from './TailwindCss.svelte';

	var options = {
		strings: ['The Land of the Gods', 'The Land of Hill Stations'],
		typeSpeed: 40,
		loop: true,
		showCursor: false
	}

	onMount(() => {
		var typed = new Typed('.typing', options)
	})
</script>
<TailwindCss/>

<style>
	a:hover {
		text-decoration: none;
	}

	a {
		color: white;
	}
</style>

<body>
	<header class="text-gray-500 bg-blue-700 body-font" id="top">
		<div class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center">
			<nav class="flex lg:w-2/5 flex-wrap items-center text-base md:ml-auto">
			  <a href="#hero" class="mr-5 hover:text-white">Home</a>
			  <a href="#places" class="mr-5 hover:text-white">Places to Visit</a>
			  <a href="#map" class="mr-5 hover:text-white">Map of Uttarakhand</a>
			  <a href="#faq" class="mr-5 hover:text-white">FAQ</a>
			</nav>
		  <a href="/" class="flex order-first lg:order-none lg:w-1/5 title-font font-semibold items-center text-white lg:items-center lg:justify-center mb-4 md:mb-0">
			<Icon/>
			<span class="ml-3 text-xl text-white">UK Tourism</span>
		  </a>
		  <div class="lg:w-2/5 inline-flex lg:justify-end ml-5 lg:ml-0">
			<button class="inline-flex items-center bg-white border-0 py-1 px-3 focus:outline-none hover:bg-gray-300 rounded text-black mt-4 md:mt-0">Button
			  <svg fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-4 h-4 ml-1" viewBox="0 0 24 24">
				<path d="M5 12h14M12 5l7 7-7 7"></path>
			  </svg>
			</button>
		  </div>
		</div>
	  </header>

	  <section class="text-gray-500 bg-blue-700 body-font">
		<div class="container mx-auto flex px-5 py-24 md:flex-row flex-col items-center">
		  <div class="lg:flex-grow md:w-1/2 lg:pr-24 md:pr-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-center text-center">
			<h1 class="inline title-font sm:text-4xl text-3xl mb-4 font-medium text-white typing">
			</h1>
		  </div>
		  <div class="lg:max-w-lg lg:w-full md:w-1/2 w-5/6">
			<img class="object-cover object-center rounded" alt="hero" src="https://static.toiimg.com/photo/72885514/Auli.jpg?width=748&resize=4">
		  </div>
		</div>
	  </section>
</body>