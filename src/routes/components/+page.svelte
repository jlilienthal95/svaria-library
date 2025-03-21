<!-- DEV NOTES:
    to add a component to the page:
    1. create the docs and add it in src/routes/components/lib
    2. create the demo and add it to src/componentDemoCode
    3. create the sandbox in the svelte REPL and save the url
    4. import in the docs to this page
    5. add it to components array
-->

<script lang="ts">
	import Sandbox from '../../FrontendComponents/ComponentsPage/Sandbox.svelte';
	import type { CompObj } from './../../types.js';

	// ======================> Component Imports < ========================
	import ButtonDocs from './lib/ButtonDocs.svelte';
	import AccordionDocs from './lib/AccordionDocs.svelte';
	import AccordionGroupDocs from './lib/AccordionGroupDocs.svelte';
	import CheckboxDocs from './lib/CheckboxDocs.svelte';
	import FormDocs from './lib/FormDocs.svelte';
	import MenuDocs from './lib/MenuDocs.svelte';
	import ModalDocs from './lib/ModalDocs.svelte';
	import NavigationDocs from './lib/NavigationDocs.svelte';
	import PopoverDocs from './lib/PopoverDocs.svelte';
	import ProgressBarDocs from './lib/ProgressBarDocs.svelte';
	import RadioGroupDocs from './lib/RadioGroupDocs.svelte';
	import SpinButtonDocs from './lib/SpinButtonDocs.svelte';
	import SwitchDocs from './lib/SwitchDocs.svelte';
	import TabDocs from './lib/TabDocs.svelte';
	import TreeDocs from './lib/TreeDocs.svelte';
	import AlertDocs from './lib/AlertDocs.svelte';
	import ToastDocs from './lib/ToastDocs.svelte';
	import MobileNav from '../../FrontendComponents/Layout/MobileNav.svelte';
	// ====================================================================

	const componentsArray: CompObj[] = [
		{
			docs: ButtonDocs,
			label: 'Button',
			source: 'https://svelte.dev/repl/3de22bc71e6c42f680c0e5dc80b42ba1?version=4.2.18'
		},
		{
			docs: AccordionDocs,
			label: 'Accordion',
			source: 'https://svelte.dev/repl/8391f5d6f9fb4cafbdc6de9dc24624b6?version=4.2.18'
		},
		{
			docs: AccordionGroupDocs,
			label: 'Accordion Group',
			source: 'https://svelte.dev/repl/6f215987234e471fbe241df938789695?version=4.2.18'
		},
		{
			docs: AlertDocs,
			label: 'Alert',
			source: 'https://svelte.dev/repl/1161a113613840b1b765e384e734eadf?version=4.2.18'
		},
		{
			docs: CheckboxDocs,
			label: 'Checkbox',
			source: 'https://svelte.dev/repl/1655765010ce4ec287f1a41a92e0a42b?version=4.2.18'
		},
		{
			docs: FormDocs,
			label: 'Form',
			source: 'https://svelte.dev/repl/e390654778f54982875cae674e39f646?version=4.2.18'
		},
		{
			docs: MenuDocs,
			label: 'Menu',
			source: 'https://svelte.dev/repl/cfc5475329ec4bf7a39597d7ed304629?version=4.2.18'
		},
		{
			docs: ModalDocs,
			label: 'Modal',
			source: 'https://svelte.dev/repl/67d050ac1ddd41d2be31d5921d29e288?version=4.2.18'
		},
		{
			docs: NavigationDocs,
			label: 'Navigation',
			source: 'https://svelte.dev/repl/88f0fc1e880a4903bb30148c1beb52ba?version=4.2.18'
		},
		{
			docs: PopoverDocs,
			label: 'Popover',
			source: 'https://svelte.dev/repl/326ee2b9cc0f445c82354b2c166b58b4?version=4.2.18'
		},
		{
			docs: ProgressBarDocs,
			label: 'Progress Bar',
			source: 'https://svelte.dev/repl/8b768afeb4d0453da297275d2132dcf3?version=4.2.18'
		},
		{
			docs: RadioGroupDocs,
			label: 'Radio Group',
			source: 'https://svelte.dev/repl/a156fc8b39454aa7a573881f334a88b5?version=4.2.18'
		},
		{
			docs: SpinButtonDocs,
			label: 'Spin Button',
			source: 'https://svelte.dev/playground/4e17f413de0c4adfbe18199f3afd761d?version=5.24.1'
		},
		{
			docs: SwitchDocs,
			label: 'Switch',
			source: 'https://svelte.dev/repl/3d98cb99b89f476ebca51f5be484dde8?version=4.2.18'
		},
		{
			docs: TabDocs,
			label: 'Tabs',
			source: 'https://svelte.dev/repl/1bc4a75b73964591800ba13f44417a3b?version=4.2.18'
		},
		{
			docs: ToastDocs,
			label: 'Toast',
			source: 'https://svelte.dev/repl/dce213fa6c084fc193244bebd34900c9?version=4.2.18'
		},
		{
			docs: TreeDocs,
			label: 'Tree',
			source: 'https://svelte.dev/repl/d18158eaa68a450aa62e8e4ae6c98f75?version=4.2.18'
		}
	];
	let component: CompObj = componentsArray[0];
	const handleClick = (comp: CompObj): void => {
		component = comp;
	};


	// ======================> drop down menu for small screens < =============

	// let menuItems = [
	// 	{
	// 		label: 'Button',
	// 		link: 'https://svelte.dev/repl/3de22bc71e6c42f680c0e5dc80b42ba1?version=4.2.18',
	// 		onClick: handleClick,
	// 		linkID: 'Button',
	// 		linkClass: 'text-white'
	// 	},
	// 	{
	// 		label: 'blue',
    //   linkID: 'blue',
			
	// 		linkClass: 'text-blue-800'
	// 	},
	// 	{
	// 		label: 'yellow',
    //   linkID: 'yellow',
			
	// 		linkClass: 'text-yellow-800'
	// 	},
	// 	{
	// 		label: 'green',
	// 		link: "https://en.wikipedia.org/wiki/Green",
    //   linkID: 'green',
	// 		linkClass: 'text-green-800'
	// 	}
	// ];
</script>

<MobileNav/>

<div id='bigScreenComponentPage' class="flex w-full">
	<aside id="default-sidebar" class="flex-shrink-0 w-64 h-screen overflow-y-auto">
		<ul class="py-4 font-medium">
			{#each componentsArray as comp}
				<li>
					<button
						class="block w-full px-4 py-2 text-left text-2xl hover:bg-gray-300"
						on:click={() => handleClick(comp)}
					>
						{comp.label}
					</button>
				</li>
			{/each}
		</ul>
	</aside>

	<div class="flex flex-col w-full xl:max-w-[60vw] max-w-[80vw] justify-center mx-6 p-1">
		<h1 id='HeaderWithIcons' class="flex w-fit text-4xl pb-6 sm:text-5xl md:text-6xl max-w-[1000px] mx-auto font-semibold text-center z-10">
			SvARIA Playground
		</h1>
		
		<Sandbox source={component.source} label={component.label}/>
		<svelte:component this={component.docs} />
	</div>
</div>
<!-- ================> drop down menu for small screens < ============= -->
<!-- <div id='smallScreenComponentPage'>
	<Menu
			{menuItems}
			buttonContent="Menu"
			buttonId="menuButton"
			buttonAriaLabel="menu button"
			buttonClass="w-32 h-9 text-xl bg-blue-300 rounded-md items-center justify-between px-3 text-gray-900 hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-black md:dark:hover:text-blue-500 dark:focus:text-black dark:hover:bg-gray-700 md:dark:hover:bg-transparent"
			listId='menuItems'
			listClass="bg-blue-200 text-lg w-32 text-center	rounded-md"
		/>
		<div class="ml-6 mr-96 p-1 flex-1 ">
			<h1 id='HeaderWithIcons' class="text-4xl ml-6 sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center relative z-10">
				<img class="SandboxImage" alt="Sandbox Icon" src={sandboxicon} />
				SvARIA Playground
				<img class="SandboxImage" alt="Sandbox Icon" src={sandboxicon} />
			</h1>
			
			<Sandbox source={component.link} label={component.label}/>
			<svelte:component this={component.docs} />
		</div>
</div>	 -->
<!-- ================> small screens component page < ============= -->
<!-- <div id='landscapeComponentChoice'>
Choose a component below:
</div>	
<div id='smallScreenComponentPage' class="flex">
	<aside id="smallSidebar" class="w-screen overflow-x-auto">
		<ul class="px-4 flex font-small">
			{#each componentsArray as comp}
				<li>
					<button
						class="block w-32 py-4 px-2 text-center text-sm hover:bg-gray-300"
						on:click={() => handleClick(comp)}
					>
						{comp.label}
					</button>
				</li>
			{/each}
		</ul>
	</aside>
	<br>
	<div class="mr-96 p-1 flex-1 ">
		<h1 id='smallHeaderWithIcons' class="text-4xl ml-6 sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center relative z-10">
			<img class="SandboxImage" alt="Sandbox Icon" src={sandboxicon} />
			SvARIA Playground
			<img class="SandboxImage" alt="Sandbox Icon" src={sandboxicon} />
		</h1>
		<br>
		<Sandbox source={component.source} label={component.label}/>
		<svelte:component this={component.docs} />
	</div>
</div>

	
<div id='portraitOverlay' >
	<h1 class='text-white text-center text-3xl mt-14'>
		Please rotate your phone to landscape
	</h1>
	<img alt="Switch phone from portrait to landscape" src={landscapePhoneSwitch} />
</div> -->