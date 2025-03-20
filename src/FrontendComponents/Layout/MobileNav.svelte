<script lang='ts'>
	import { fly, slide, fade } from 'svelte/transition';
    import { openModal } from '../../store';
	import { bounceIn } from 'svelte/easing';


    function reroute(href: string) {
		$openModal = false;
		window.location.href = href;
	}

</script>

{#if $openModal}
    <div
        id='MobileNav'
        class="fixed top-0 left-0 w-screen h-screen border-b bg-white z-50 flex flex-col gap-8 px-8 lg:hidden"
    >
        <div id="MobileHeader" class="flex items-center justify-between gap-4 border-b pb-4">
            <a id="MobileLogo" href="/">
                <img class="min-w-[250px] h-[125px] w-[250px]" alt="SvARIA Logo" src="/SvAriaLogo.png" />
            </a>
            <button
                id="closeButton"
                class="outline-none border-none"
                aria-label = "Close Menu"
                on:click={() => {
                    $openModal = false;
                }}
            >
            <i class="fa-solid fa-xmark text-5xl pr-6"></i>
            </button>
        </div>
        <div id="MobileLinks" class="flex flex-col gap-4 flex-1" out:fade={{duration: 250}}>
            <button
                in:fly={{duration: 750, x: -100}}
                on:click={() => reroute('/#WhySvARIA')}
                class="border-none outline-none p-2 group duration-200 cursor-pointer text-left"
            >
                <p class="duration-200 group-hover:pl-2 poppins text-3xl font-semibold">
                    Why SvARIA <i class="fa-solid fa-chevron-right text-xl pl-4"></i>
                </p>
            </button>
            <button
                in:fly={{duration: 750, delay: 150, x: -100}}
                on:click={() => reroute('/#GettingStarted')}
                class="border-none outline-none p-2 group duration-200 cursor-pointer text-left"
            >
                <p class="duration-200 group-hover:pl-2 poppins text-3xl font-semibold">
                    Getting Started <i class="fa-solid fa-chevron-right text-xl pl-4"></i>
                </p>
            </button>
            <button
                in:fly={{duration: 750, delay: 300, x: -100}}
                on:click={() => reroute('/components')}
                class="border-none outline-none p-2 group duration-200 cursor-pointer text-left"
            >
                <p class="duration-200 group-hover:pl-2 poppins text-3xl font-semibold">
                    Components <i class="fa-solid fa-chevron-right text-xl pl-4"></i>
                </p>
            </button>
            <button
                in:fly={{duration: 750, delay: 450, x: -100}}
                on:click={() => reroute('https://github.com/oslabs-beta/SvARIA')}
                class="border-none outline-none p-2 group duration-200 cursor-pointer text-left"
            >
                <p class="duration-200 group-hover:pl-2 poppins text-3xl font-semibold">
                    GitHub <i class="fa-solid fa-chevron-right text-xl pl-4"></i>
                </p>
            </button>
            <button
                in:fly={{duration: 750, delay: 600, x: -100}}
                on:click={() => reroute('/#News')}
                class="border-none outline-none p-2 group duration-200 cursor-pointer text-left"
            >
                <p class="duration-200 group-hover:pl-2 poppins text-3xl font-semibold">
                    News <i class="fa-solid fa-chevron-right text-xl pl-4"></i>
                </p>
            </button>
        </div>
    </div>
{/if}