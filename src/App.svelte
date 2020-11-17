<script>
	import Icon from './Icon.svelte';
	import TailwindCss from './TailwindCss.svelte';
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
	<header class="text-gray-500 bg-blue-500 body-font" id="top">
		<div class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center">
		  <a href="/" class="no-underline flex title-font font-medium items-center text-white mb-4 md:mb-0 atag">
			<Icon/>
			<span class="ml-3 text-2xl text-white">Uttarakhand Tourism</span>
		  </a>
		  <nav class="md:mr-auto md:ml-4 md:py-1 md:pl-4 md:border-l md:border-gray-700	flex flex-wrap items-center text-base justify-center">
			<a href="#hero" class="mr-5 text-2xl text-white hover:text-white">Home</a>
			<a href="#places" class="mr-5 text-2xl text-white hover:text-white">Places to Visit</a>
			<a href="#map" class="mr-5 text-2xl text-white hover:text-white">Map of Uttarakhand</a>
			<a href="#faq" class="mr-5 text-2xl text-white hover:text-white">FAQ</a>
		  </nav>
		</div>
	  </header>
</body>