<svelte:head>
	<link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css"
	integrity="sha512-xodZBNTC5n17Xt2atTPuE1HxjVMSvLVW9ocqUKLsCC5CXdbqCmblAshOMAS6/keqq/sMZMZ19scR4PsZChSR7A=="
	crossorigin=""/>
</svelte:head>

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
		var mymap = L.map("map").setView([29.3919, 79.4542], 13);
		L.tileLayer(
		"https://api.mapbox.com/styles/v1/{id}/tiles/{z}/{x}/{y}?access_token={accessToken}",
		{
			attribution:
			'Map data &copy; <a href="https://www.openstreetmap.org/">OpenStreetMap</a> contributors, <a href="https://creativecommons.org/licenses/by-sa/2.0/">CC-BY-SA</a>, Imagery © <a href="https://www.mapbox.com/">Mapbox</a>',
			maxZoom: 18,
			id: "mapbox/streets-v11",
			tileSize: 512,
			zoomOffset: -1,
			accessToken:
			"pk.eyJ1IjoiY2hhcnRzdHVkaW91c2VyIiwiYSI6ImNrZXd3bTBoNTA4bnYyemw4N3l5aDN5azIifQ.7e-KoC1KMXr_EKbkahgAQQ",
		}
		).addTo(mymap);

		L.marker([30.3165, 78.0322]).addTo(mymap).bindPopup("Dehradun").openPopup();
		L.marker([30.4598, 78.0644]).addTo(mymap).bindPopup("Mussoorie").openPopup();
		L.marker([29.3919, 79.4542]).addTo(mymap).bindPopup("Nainital").openPopup();
		L.marker([30.0869, 78.2676]).addTo(mymap).bindPopup("Rishikesh").openPopup();
		L.marker([29.5300, 78.7747]).addTo(mymap).bindPopup("Jim Corbett National Park").openPopup();
		L.marker([30.52892, 79.57026]).addTo(mymap).bindPopup("Auli").openPopup();
		L.marker([30.2937, 79.5603]).addTo(mymap).bindPopup("Chamoli").openPopup();
		L.marker([29.8377, 78.6871]).addTo(mymap).bindPopup("Lansdowne").openPopup();
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
				<a href="#faq" class="mr-5 hover:text-white">FAQ</a>
			</nav>
        </div>
	</header>
	<!-- Must Change Section Hero Later -->
    <section id="hero" class="text-gray-500 bg-gray-900 body-font">
		<div class="container mx-auto flex px-5 py-24 md:flex-row flex-col items-center">
		  <div class="lg:flex-grow md:w-1/2 lg:pr-24 md:pr-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-center text-center">
			<h1 class="title-font sm:text-4xl text-3xl mb-4 font-medium text-white">Uttarakhand
			  <br class="hidden lg:inline-block">The Land of Gods
			</h1>
			<p class="mb-8 leading-relaxed">
				On the foothills of Himalayas, there is an enchanting land named Uttarakhand, which adds five stars to the beauty of Northern India.
				Mysterious, beautiful, exotic, charming, and magnificent, that’s Uttarakhand in a nutshell. 
			</p>
		  </div>
		  <div class="lg:max-w-lg lg:w-full md:w-1/2 w-5/6">
			<img class="object-cover object-center rounded" alt="hero" src="https://images.indianexpress.com/2020/09/uttarakhand-1200.jpg">
		  </div>
		</div>
	  </section>
	  <!-- Places to Visit Section -->
	  <section id="places" class="text-gray-500 body-font bg-gray-900">
		<div class="container px-5 py-24 mx-auto">
		  <div class="flex flex-wrap w-full mb-20">
			<div class="lg:w-1/2 w-full mb-6 lg:mb-0">
			  <h1 class="sm:text-3xl text-2xl font-medium title-font mb-2 text-white">Places to Visit</h1>
			  <div class="h-1 w-20 bg-indigo-500 rounded"></div>
			</div>
			<p class="lg:w-1/2 w-full leading-relaxed text-base">
				They call it the ‘Land of Gods’. The enchanting land is blessed with some amazing tourist places and when you visit this place you can better judge why the Gods chose Uttrakhand to make it their abode. With several beautiful places to visit in Uttarakhand, a trip to Uttarakhand should definitely be in your bucket list of places to see in India. If you are already on your way to plan a trip, here is a list of places to visit in Uttarakhand.
			</p>
		  </div>
		  <div class="flex flex-wrap -m-4">
			<div class="xl:w-1/4 md:w-1/2 p-4">
			  <div class="bg-gray-800 p-6 rounded-lg">
				<img class="h-40 rounded w-full object-cover object-center mb-6" src="https://uttarakhandtourism.gov.in/wp-content/uploads/2018/11/dehradun-2-300x200.jpg" alt="content">
				<h3 class="tracking-widest text-indigo-500 text-xs font-medium title-font">BETWEEN MARCH AND JUNE</h3>
				<h2 class="text-lg text-white font-medium title-font mb-4">Dehradun</h2>
				<p class="leading-relaxed text-base">Shop for pretty woollens, handicrafts, handlooms, juices, jams, jellies and clothes in the local market. Don’t forget to try out the delicious Garhwali food at the local restaurants.</p>
			  </div>
			</div>
			<div class="xl:w-1/4 md:w-1/2 p-4">
			  <div class="bg-gray-800 p-6 rounded-lg">
				<img class="h-40 rounded w-full object-cover object-center mb-6" src="https://uttarakhandtourism.gov.in/wp-content/uploads/2018/11/destination-mussoorie-300x200.jpg" alt="content">
				<h3 class="tracking-widest text-indigo-500 text-xs font-medium title-font">BETWEEN APRIL AND JUNE</h3>
				<h2 class="text-lg text-white font-medium title-font mb-4">Mussoorie</h2>
				<p class="leading-relaxed text-base">Walk through the winding lanes of the tiny town and explore its beauty. Also, try your luck in spotting resident author Ruskin Bond, who enjoys a stroll through the markets.</p>
			  </div>
			</div>
			<div class="xl:w-1/4 md:w-1/2 p-4">
			  <div class="bg-gray-800 p-6 rounded-lg">
				<img class="h-40 rounded w-full object-cover object-center mb-6" src="https://uttarakhandtourism.gov.in/wp-content/uploads/2018/11/nainital-2-300x200.jpg" alt="content">
				<h3 class="tracking-widest text-indigo-500 text-xs font-medium title-font">BETWEEN MARCH AND JUNE</h3>
				<h2 class="text-lg text-white font-medium title-font mb-4">Nainital</h2>
				<p class="leading-relaxed text-base">Shop for woollens, handicrafts, jewellery and soveniour in the shops on Mall Road. If you love adventure, then there are options for trekking.</p>
			  </div>
			</div>
			<div class="xl:w-1/4 md:w-1/2 p-4">
			  <div class="bg-gray-800 p-6 rounded-lg">
				<img class="h-40 rounded w-full object-cover object-center mb-6" src="https://uttarakhandtourism.gov.in/wp-content/uploads/2018/11/destination-rishikesh-300x200.jpg" alt="content">
				<h3 class="tracking-widest text-indigo-500 text-xs font-medium title-font">BETWEEN AUGUST AND OCTOBER</h3>
				<h2 class="text-lg text-white font-medium title-font mb-4">Rishikesh</h2>
				<p class="leading-relaxed text-base">A thrilling white water rafting in Rishikesh is an experience of a lifetime. Looking for a divine experience? Take a dip in the holy Ganga and feel spiritually cleansed.</p>
			  </div>
			</div>
			<div class="xl:w-1/4 md:w-1/2 p-4">
				<div class="bg-gray-800 p-6 rounded-lg">
				  <img class="h-40 rounded w-full object-cover object-center mb-6" src="https://uttarakhandtourism.gov.in/wp-content/uploads/2018/11/destination-corbett-300x200.jpg" alt="content">
				  <h3 class="tracking-widest text-indigo-500 text-xs font-medium title-font">DEPENDS ON YOUR INTERESTS</h3>
				  <h2 class="text-lg text-white font-medium title-font mb-4">Jim Corbett National Park</h2>
				  <p class="leading-relaxed text-base">Jim Corbett National Park is a forested wildlife sanctuary in northern India’s Uttarakhand State. Rich in flora and fauna, it’s known for its Bengal tigers. Animals, including tigers, leopards and wild elephants, roam the Dhikala zone.</p>
				</div>
			  </div>
			  <div class="xl:w-1/4 md:w-1/2 p-4">
				<div class="bg-gray-800 p-6 rounded-lg">
				  <img class="h-40 rounded w-full object-cover object-center mb-6" src="https://uttarakhandtourism.gov.in/wp-content/uploads/2018/11/auli-300x200.jpeg" alt="content">
				  <h3 class="tracking-widest text-indigo-500 text-xs font-medium title-font">ANYTIME OF THE YEAR</h3>
				  <h2 class="text-lg text-white font-medium title-font mb-4">Auli</h2>
				  <p class="leading-relaxed text-base">Auli is the skiing and snowboarding hub of India. You can try your hand at skiing here. There are different courses to learn the sport. Try your lick at mountaineering here and you will have an unforgettable experience. Winters can be extremely cold and you will need to bundle up.</p>
				</div>
			  </div>
			  <div class="xl:w-1/4 md:w-1/2 p-4">
				<div class="bg-gray-800 p-6 rounded-lg">
				  <img class="h-40 rounded w-full object-cover object-center mb-6" src="https://uttarakhandtourism.gov.in/wp-content/uploads/2018/11/chamoli-1-300x200.jpg" alt="content">
				  <h3 class="tracking-widest text-indigo-500 text-xs font-medium title-font">BETWEEN OCTOBER AND MARCH</h3>
				  <h2 class="text-lg text-white font-medium title-font mb-4">Chamoli</h2>
				  <p class="leading-relaxed text-base">Enjoy the cable car ride here. The ride is very scenic and enjoyable. Trekking is another option to indulge in this wonderful town.</p>
				</div>
			  </div>
			  <div class="xl:w-1/4 md:w-1/2 p-4">
				<div class="bg-gray-800 p-6 rounded-lg">
				  <img class="h-40 rounded w-full object-cover object-center mb-6" src="https://uttarakhandtourism.gov.in/wp-content/uploads/2018/12/destination-lansdown-300x200.jpg" alt="content">
				  <h3 class="tracking-widest text-indigo-500 text-xs font-medium title-font">BETWEEN JULY AND SEPTEMBER</h3>
				  <h2 class="text-lg text-white font-medium title-font mb-4">Lansdowne</h2>
				  <p class="leading-relaxed text-base">Enjoy a peaceful walk or simply sit and stare at the beauty of nature. You can also go on the forest trail to explore the wilderness of this beautiful place.</p>
				</div>
			  </div>
		  </div>
		</div>
	  </section>
	  <section id="map"></section>
	  <!-- FAQ Section -->
	  <section id="faq" class="text-gray-500 bg-gray-900 body-font overflow-hidden">
		<div class="container px-5 py-24 mx-auto">
		  <div class="-my-8">
			<div class="py-8 flex flex-wrap md:flex-no-wrap">
			  <div class="md:flex-grow">
				<h2 class="text-2xl font-medium text-white title-font mb-2">1. What adventure activities are there in Uttarakhand?</h2>
				<p class="leading-relaxed">Uttarakhand is a gold mine of adventure activities. From varying intensity treks, skiing, and paragliding to white water rafting and camping, there are enough activities for the adventure junkie in you to explore and experience.</p>
			  </div>
			</div>
			<div class="py-8 flex border-t-2 border-gray-800 flex-wrap md:flex-no-wrap">
			  <div class="md:flex-grow">
				<h2 class="text-2xl font-medium text-white title-font mb-2">2. What is the best time to visit Uttarakhand?</h2>
				<p class="leading-relaxed">You can visit Uttarakhand all year long and the experience will be thrilling. However, summertime from March through June and winter days from October to February is supposed to be the best time to visit. The weather is pleasant and is sure to give you the most amazing vacation feels.</p>
			  </div>
			</div>
			<div class="py-8 flex border-t-2 border-gray-800 flex-wrap md:flex-no-wrap">
			  <div class="md:flex-grow">
				<h2 class="text-2xl font-medium text-white title-font mb-2">3. What can I expect while visiting Uttarakhand?</h2>
				<p class="leading-relaxed">Traveling to Uttarakhand, you can expect to feel the spiritual powers of the mountains reverberating as you drive down the treacherous roads or trek the mighty mountains. The scenic beauty is overwhelming and feels as close to paradise as it can get. You can surely expect to feel rejuvenated and replenished after a visit to this glorious place.</p>
			  </div>
			</div>
		  </div>
		</div>
	  </section>
	  <!-- The Footer Section -->
	  <footer class="text-gray-500 bg-gray-900 body-font">
		<div class="container px-5 py-8 mx-auto flex justify-center items-center sm:flex-row flex-col">
		  <a href="#hero" class="flex title-font font-medium items-center md:justify-start justify-center text-white">
			<Icon/>
			<span class="ml-3 text-xl">UK Tourism</span>
		  </a>
		  <p class="text-lg text-gray-600 sm:ml-4 sm:pl-4 sm:border-l-2 sm:border-gray-800 sm:py-2 sm:mt-0 mt-4">© 2020 UK Tourism
		  </p>
		</div>
	  </footer>
</body>

