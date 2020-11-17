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
	<header class="text-gray-500 bg-blue-400 body-font" id="top">
		<div class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center">
		  <a href="/" class="flex title-font font-medium items-center text-white mb-4 md:mb-0">
			<Icon/>
			<span class="ml-3 text-xl text-white">Uttarakhand Tourism</span>
		  </a>
		  <nav class="md:ml-auto md:mr-auto flex flex-wrap items-center text-base justify-center">
			<a href="#hero" class="mr-5 hover:text-white">Home</a>
			<a href="#places" class="mr-5 hover:text-white">Places to Visit</a>
			<a href="#map" class="mr-5 hover:text-white">Map of Uttarakhand</a>
			<a href="#faq" class="mr-5 hover:text-white">FAQ</a>
		  </nav>
		</div>
	  </header>
</body>