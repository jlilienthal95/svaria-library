<script>
    import "../app.css";
    import { derived, writable } from "svelte/store";
    // import ChatBotContainer from './components/lib/ChatBotContainer.svelte';
	import MobileNav from "../FrontendComponents/Layout/MobileNav.svelte";
    import Navbar from "../FrontendComponents/Layout/Navbar.svelte";
    import Footer from "../FrontendComponents/Layout/Footer.svelte";
	import { fade, slide } from "svelte/transition";
	let { children } = $props();

//these variables track page scrolling and are used to prompt header to fade in at fixed position
	//scrollY tracks current vertical scroll value
	const scrollY = writable(0);
	//innerHeight tracks initial viewport
	const innerHeight = writable(0);

    const showNavBar = derived([scrollY, innerHeight], ([$scrollY, $innerHeight]) => $scrollY > $innerHeight - 100);
</script>


<MobileNav />

<div class="top-0 left-0 w-full flex flex-col z-20 bg-white">
    <Navbar />
</div>

{#if $showNavBar}
    <div class="fixed top-0 left-0 w-full flex bg-white flex-col z-20 px-4" in:fade={{ duration: 500}} out:slide={{ duration: 500}}>
        <Navbar />
    </div>
{/if}

<div id="mainContent" class="h-full w-full bg-white">
    {@render children()}
</div>

<!-- <ChatBotContainer /> -->
<div class="bottom-0 left-0 w-full flex flex-col z-20 relative">
    <Footer />
</div>

<svelte:window bind:scrollY={$scrollY} bind:innerHeight={$innerHeight} />