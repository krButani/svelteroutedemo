<script>
	import  Router from 'svelte-spa-router';
	import {location,link} from 'svelte-spa-router';
	import About from './view/about.svelte';
	import Book from './view/book.svelte';
	import Home from './view/Home.svelte';

	let routes = {
		"/": Home,
		"/about": About,
		"/book/:id": Book
	}
</script>

<nav>
	<a use:link href="/">Home</a>
	<a use:link href="/about">About</a>
	<a use:link href="/book/155/">Book</a>
</nav>
<main>
<Router routes={routes} />
<h2>Current Location {$location}</h2>
</main>



