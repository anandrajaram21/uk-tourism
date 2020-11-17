<script>
    import { onMount } from 'svelte';
	import Icon from './Icon.svelte';
    import Typed from 'typed.js';
	import TailwindCss from './TailwindCss.svelte';
	import * as L from 'leaflet';
    
    var options = {
    	strings: ['The Land of the Gods', 'The Land of Hill Stations'],
    	typeSpeed: 40,
    	loop: true,
    	showCursor: false
	}

    onMount(() => {
		// var typed = new Typed('.typing', options);
		var mymap = L.map("map").setView([30.0668, 79.0193], 13);
		L.tileLayer(
		"https://api.mapbox.com/styles/v1/{id}/tiles/{z}/{x}/{y}?access_token={accessToken}",
		{
			attribution:
			'Map data &copy; <a href="https://www.openstreetmap.org/">OpenStreetMap</a> contributors, <a href="https://creativecommons.org/licenses/by-sa/2.0/">CC-BY-SA</a>, Imagery © <a href="https://www.mapbox.com/">Mapbox</a>',
			maxZoom: 18,
			id: "mapbox/dark-v10",
			tileSize: 512,
			zoomOffset: -1,
			accessToken:
			"pk.eyJ1IjoiY2hhcnRzdHVkaW91c2VyIiwiYSI6ImNrZXd3bTBoNTA4bnYyemw4N3l5aDN5azIifQ.7e-KoC1KMXr_EKbkahgAQQ",
		}
		).addTo(mymap);

		L.marker([29.3919, 79.4542]).addTo(mymap)
    })
</script>

<svelte:head>
	<link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css"
	integrity="sha512-xodZBNTC5n17Xt2atTPuE1HxjVMSvLVW9ocqUKLsCC5CXdbqCmblAshOMAS6/keqq/sMZMZ19scR4PsZChSR7A=="
	crossorigin=""/>
</svelte:head>

<TailwindCss/>

<style>
    a:hover {
    text-decoration: none;
    }

    a {
    color: white;
	}
	
	#map {
		width: 100%;
		height: 32em;
	}
</style>

<body>
    <header class="text-gray-500 bg-gray-900 body-font" id="top">
        <div class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center">
            <a href="/" class="flex title-font font-medium items-center text-white mb-4 md:mb-0">
                <Icon/>
                <span class="ml-3 text-xl text-white">UK Tourism</span>
            </a>
			<nav class="md:ml-auto flex flex-wrap items-center text-base justify-center">
				<a href="#hero" class="mr-5 hover:text-white">Home</a>
				<a href="#places" class="mr-5 hover:text-white">Places to Visit</a>
				<a href="#map" class="mr-5 hover:text-white">Map of Uttarakhand</a>
				<a href="#gallery" class="mr-5 hover:text-white">Gallery</a>
				<a href="#faq" class="mr-5 hover:text-white">FAQ</a>
			</nav>
        </div>
	</header>
	<!-- Must Change Section Hero Later -->
    <section id="hero" class="text-gray-500 bg-gray-900 body-font">
		<div class="container mx-auto flex px-5 py-24 md:flex-row flex-col items-center">
		  <div class="lg:flex-grow md:w-1/2 lg:pr-24 md:pr-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-center text-center">
			<h1 class="title-font sm:text-4xl text-3xl mb-4 font-medium text-white">Before they sold out
			  <br class="hidden lg:inline-block">readymade gluten
			</h1>
			<p class="mb-8 leading-relaxed">Copper mug try-hard pitchfork pour-over freegan heirloom neutra air plant cold-pressed tacos poke beard tote bag. Heirloom echo park mlkshk tote bag selvage hot chicken authentic tumeric truffaut hexagon try-hard chambray.</p>
			<div class="flex justify-center">
			  <button class="inline-flex text-white bg-indigo-500 border-0 py-2 px-6 focus:outline-none hover:bg-indigo-600 rounded text-lg">Button</button>
			  <button class="ml-4 inline-flex text-gray-400 bg-gray-800 border-0 py-2 px-6 focus:outline-none hover:bg-gray-700 hover:text-white rounded text-lg">Button</button>
			</div>
		  </div>
		  <div class="lg:max-w-lg lg:w-full md:w-1/2 w-5/6">
			<img class="object-cover object-center rounded" alt="hero" src="https://dummyimage.com/720x600">
		  </div>
		</div>
	  </section>
	  <!-- Places to Visit Section -->
	  <section id="places" class="text-gray-500 body-font bg-gray-900">
		<div class="container px-5 py-24 mx-auto">
		  <div class="flex flex-wrap w-full mb-20">
			<div class="lg:w-1/2 w-full mb-6 lg:mb-0">
			  <h1 class="sm:text-3xl text-2xl font-medium title-font mb-2 text-white">Pitchfork Kickstarter Taxidermy</h1>
			  <div class="h-1 w-20 bg-indigo-500 rounded"></div>
			</div>
			<p class="lg:w-1/2 w-full leading-relaxed text-base">Whatever cardigan tote bag tumblr hexagon brooklyn asymmetrical gentrify, subway tile poke farm-to-table. Franzen you probably haven't heard of them man bun deep jianbing selfies heirloom prism food truck ugh squid celiac humblebrag.</p>
		  </div>
		  <div class="flex flex-wrap -m-4">
			<div class="xl:w-1/4 md:w-1/2 p-4">
			  <div class="bg-gray-800 p-6 rounded-lg">
				<img class="h-40 rounded w-full object-cover object-center mb-6" src="https://dummyimage.com/720x400" alt="content">
				<h3 class="tracking-widest text-indigo-500 text-xs font-medium title-font">SUBTITLE</h3>
				<h2 class="text-lg text-white font-medium title-font mb-4">Chichen Itza</h2>
				<p class="leading-relaxed text-base">Fingerstache flexitarian street art 8-bit waistcoat. Distillery hexagon disrupt edison bulbche.</p>
			  </div>
			</div>
			<div class="xl:w-1/4 md:w-1/2 p-4">
			  <div class="bg-gray-800 p-6 rounded-lg">
				<img class="h-40 rounded w-full object-cover object-center mb-6" src="https://dummyimage.com/721x401" alt="content">
				<h3 class="tracking-widest text-indigo-500 text-xs font-medium title-font">SUBTITLE</h3>
				<h2 class="text-lg text-white font-medium title-font mb-4">Colosseum Roma</h2>
				<p class="leading-relaxed text-base">Fingerstache flexitarian street art 8-bit waistcoat. Distillery hexagon disrupt edison bulbche.</p>
			  </div>
			</div>
			<div class="xl:w-1/4 md:w-1/2 p-4">
			  <div class="bg-gray-800 p-6 rounded-lg">
				<img class="h-40 rounded w-full object-cover object-center mb-6" src="https://dummyimage.com/722x402" alt="content">
				<h3 class="tracking-widest text-indigo-500 text-xs font-medium title-font">SUBTITLE</h3>
				<h2 class="text-lg text-white font-medium title-font mb-4">Great Pyramid of Giza</h2>
				<p class="leading-relaxed text-base">Fingerstache flexitarian street art 8-bit waistcoat. Distillery hexagon disrupt edison bulbche.</p>
			  </div>
			</div>
			<div class="xl:w-1/4 md:w-1/2 p-4">
			  <div class="bg-gray-800 p-6 rounded-lg">
				<img class="h-40 rounded w-full object-cover object-center mb-6" src="https://dummyimage.com/723x403" alt="content">
				<h3 class="tracking-widest text-indigo-500 text-xs font-medium title-font">SUBTITLE</h3>
				<h2 class="text-lg text-white font-medium title-font mb-4">San Francisco</h2>
				<p class="leading-relaxed text-base">Fingerstache flexitarian street art 8-bit waistcoat. Distillery hexagon disrupt edison bulbche.</p>
			  </div>
			</div>
		  </div>
		</div>
	  </section>
	  <!-- Map Section -->
	  <!-- <section class="text-gray-500 bg-gray-900 body-font relative">
		<div class="container px-5 py-24 mx-auto flex sm:flex-no-wrap flex-wrap">
		  <div class="lg:w-2/3 md:w-1/2 bg-gray-900 rounded-lg overflow-hidden sm:mr-10 p-10 flex items-end justify-start relative">
			<iframe title="map" class="absolute inset-0" style="filter: grayscale(1) contrast(1.2) opacity(0.16);" marginheight="0" marginwidth="0" scrolling="no" src="https://maps.google.com/maps?width=100%&amp;height=600&amp;hl=en&amp;q=%C4%B0zmir+(My%20Business%20Name)&amp;ie=UTF8&amp;t=&amp;z=14&amp;iwloc=B&amp;output=embed" width="100%" height="100%" frameborder="0"></iframe>
			<div class="bg-gray-900 relative flex flex-wrap py-6">
			  <div class="lg:w-1/2 px-6">
				<h2 class="title-font font-medium text-white tracking-widest text-sm">ADDRESS</h2>
				<p class="leading-relaxed">Photo booth tattooed prism, portland taiyaki hoodie neutra typewriter</p>
			  </div>
			  <div class="lg:w-1/2 px-6 mt-4 lg:mt-0">
				<h2 class="title-font font-medium text-white tracking-widest text-sm">EMAIL</h2>
				<a class="text-indigo-500 leading-relaxed">example@email.com</a>
				<h2 class="title-font font-medium text-white tracking-widest text-sm mt-4">PHONE</h2>
				<p class="leading-relaxed">123-456-7890</p>
			  </div>
			</div>
		  </div>
		  <div class="lg:w-1/3 md:w-1/2 flex flex-col md:ml-auto w-full md:py-8 mt-8 md:mt-0">
			<h2 class="text-white text-lg mb-1 font-medium title-font">Feedback</h2>
			<p class="leading-relaxed mb-5 text-gray-600">Post-ironic portland shabby chic echo park, banjo fashion axe</p>
			<div class="relative mb-4">
			  <label for="name" class="leading-7 text-sm text-gray-400">Name</label>
			  <input type="text" id="name" name="name" class="w-full bg-gray-800 rounded border border-gray-700 focus:border-indigo-500 text-base outline-none text-gray-100 py-1 px-3 leading-8 transition-colors duration-200 ease-in-out">
			</div>
			<div class="relative mb-4">
			  <label for="email" class="leading-7 text-sm text-gray-400">Email</label>
			  <input type="email" id="email" name="email" class="w-full bg-gray-800 rounded border border-gray-700 focus:border-indigo-500 text-base outline-none text-gray-100 py-1 px-3 leading-8 transition-colors duration-200 ease-in-out">
			</div>
			<div class="relative mb-4">
			  <label for="message" class="leading-7 text-sm text-gray-400">Message</label>
			  <textarea id="message" name="message" class="w-full bg-gray-800 rounded border border-gray-700 focus:border-indigo-500 h-32 text-base outline-none text-gray-100 py-1 px-3 resize-none leading-6 transition-colors duration-200 ease-in-out"></textarea>
			</div>
			<button class="text-white bg-indigo-500 border-0 py-2 px-6 focus:outline-none hover:bg-indigo-600 rounded text-lg">Button</button>
			<p class="text-xs text-gray-500 mt-3">Chicharrones blog helvetica normcore iceland tousled brook viral artisan.</p>
		  </div>
		</div>
	  </section> -->
	  <div id="map">

	  </div>
	  <!-- Gallery -->
	  <section id="gallery" class="text-gray-500 bg-gray-900 body-font">
		<div class="container px-5 py-24 mx-auto flex flex-wrap">
		  <div class="flex w-full mb-20 flex-wrap">
			<h1 class="sm:text-3xl text-2xl font-medium title-font text-white lg:w-1/3 lg:mb-0 mb-4">Master Cleanse Reliac Heirloom</h1>
			<p class="lg:pl-6 lg:w-2/3 mx-auto leading-relaxed text-base">Whatever cardigan tote bag tumblr hexagon brooklyn asymmetrical gentrify, subway tile poke farm-to-table. Franzen you probably haven't heard of them man bun deep jianbing selfies heirloom.</p>
		  </div>
		  <div class="flex flex-wrap md:-m-2 -m-1">
			<div class="flex flex-wrap w-1/2">
			  <div class="md:p-2 p-1 w-1/2">
				<img alt="gallery" class="w-full object-cover h-full object-center block" src="https://dummyimage.com/500x300">
			  </div>
			  <div class="md:p-2 p-1 w-1/2">
				<img alt="gallery" class="w-full object-cover h-full object-center block" src="https://dummyimage.com/501x301">
			  </div>
			  <div class="md:p-2 p-1 w-full">
				<img alt="gallery" class="w-full h-full object-cover object-center block" src="https://dummyimage.com/600x360">
			  </div>
			</div>
			<div class="flex flex-wrap w-1/2">
			  <div class="md:p-2 p-1 w-full">
				<img alt="gallery" class="w-full h-full object-cover object-center block" src="https://dummyimage.com/601x361">
			  </div>
			  <div class="md:p-2 p-1 w-1/2">
				<img alt="gallery" class="w-full object-cover h-full object-center block" src="https://dummyimage.com/502x302">
			  </div>
			  <div class="md:p-2 p-1 w-1/2">
				<img alt="gallery" class="w-full object-cover h-full object-center block" src="https://dummyimage.com/503x303">
			  </div>
			</div>
		  </div>
		</div>
	  </section>
	  <!-- FAQ Section -->
	  <section id="faq" class="text-gray-500 bg-gray-900 body-font overflow-hidden">
		<div class="container px-5 py-24 mx-auto">
		  <div class="-my-8">
			<div class="py-8 flex flex-wrap md:flex-no-wrap">
			  <div class="md:flex-grow">
				<h2 class="text-2xl font-medium text-white title-font mb-2">Bitters hashtag waistcoat fashion axe chia unicorn</h2>
				<p class="leading-relaxed">Glossier echo park pug, church-key sartorial biodiesel vexillologist pop-up snackwave ramps cornhole. Marfa 3 wolf moon party messenger bag selfies, poke vaporware kombucha lumbersexual pork belly polaroid hoodie portland craft beer.</p>
				<a class="text-indigo-500 inline-flex items-center mt-4">Learn More
				  <svg class="w-4 h-4 ml-2" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round">
					<path d="M5 12h14"></path>
					<path d="M12 5l7 7-7 7"></path>
				  </svg>
				</a>
			  </div>
			</div>
			<div class="py-8 flex border-t-2 border-gray-800 flex-wrap md:flex-no-wrap">
			  <div class="md:flex-grow">
				<h2 class="text-2xl font-medium text-white title-font mb-2">Meditation bushwick direct trade taxidermy shaman</h2>
				<p class="leading-relaxed">Glossier echo park pug, church-key sartorial biodiesel vexillologist pop-up snackwave ramps cornhole. Marfa 3 wolf moon party messenger bag selfies, poke vaporware kombucha lumbersexual pork belly polaroid hoodie portland craft beer.</p>
				<a class="text-indigo-500 inline-flex items-center mt-4">Learn More
				  <svg class="w-4 h-4 ml-2" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round">
					<path d="M5 12h14"></path>
					<path d="M12 5l7 7-7 7"></path>
				  </svg>
				</a>
			  </div>
			</div>
			<div class="py-8 flex border-t-2 border-gray-800 flex-wrap md:flex-no-wrap">
			  <div class="md:flex-grow">
				<h2 class="text-2xl font-medium text-white title-font mb-2">Woke master cleanse drinking vinegar salvia</h2>
				<p class="leading-relaxed">Glossier echo park pug, church-key sartorial biodiesel vexillologist pop-up snackwave ramps cornhole. Marfa 3 wolf moon party messenger bag selfies, poke vaporware kombucha lumbersexual pork belly polaroid hoodie portland craft beer.</p>
				<a class="text-indigo-500 inline-flex items-center mt-4">Learn More
				  <svg class="w-4 h-4 ml-2" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round">
					<path d="M5 12h14"></path>
					<path d="M12 5l7 7-7 7"></path>
				  </svg>
				</a>
			  </div>
			</div>
		  </div>
		</div>
	  </section>
</body>

