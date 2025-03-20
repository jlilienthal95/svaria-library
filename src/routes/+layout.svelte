<script>
    import "../app.css";
    // import ChatBotContainer from './components/lib/ChatBotContainer.svelte';
	import MobileNav from "../FrontendComponents/Layout/MobileNav.svelte";
    import Navbar from "../FrontendComponents/Layout/Navbar.svelte";
    import Footer from "../FrontendComponents/Layout/Footer.svelte";
	let { children } = $props();
</script>

<MobileNav />

<div class="top-0 left-0 w-full flex flex-col z-20 px-4">
	<Navbar />
</div>

<div id="mainContent" class="h-full w-full">
    {@render children()}
</div>

<!-- <ChatBotContainer /> -->
<div class="bottom-0 left-0 w-full flex flex-col z-20 relative">
    <Footer />
</div>