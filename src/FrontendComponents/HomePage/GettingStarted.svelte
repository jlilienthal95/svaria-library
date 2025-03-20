<script>
	async function handleClick() {
		try {
			await navigator.clipboard.writeText('npm install svaria-toolkit');
			const copyButton = document.getElementById('toolTip');
			if(copyButton){
				copyButton.textContent = "copied!"
			}
		} catch (e) {
			console.error('Error copying to clipboard');
		}
	}
</script>

<div id="GettingStarted" class="flex flex-col gap-5 sm:gap-10 md:gap-15 items-center justify-center pt-[15vh] px-3">
	<div class="flex flex-col gap-2">
		<h4
			class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center mobileTitle"
		>
			Getting Started
		</h4>
	</div>
	<span
		class="text-xl sm:text-2xl md:text-3xl max-w-[1000px] mx-auto w-full italic font-light text-center shiftUp"
	>
		Visit the
		<a href="/components" class="text-theme-blue">
		Components Page
		</a
		> for documentation, code snippets, and interactive demos in a sandbox environment.
	</span>
	<h5 class="text-2xl sm:text-3xl md:text-4xl max-w-[1000px] mx-auto w-full text-center font-semibold mobileTitle">
		Installation
		<p
			class="text-xl sm:text-2xl md:text-3xl max-w-[1000px] mx-auto w-full italic font-light text-center"
		>
			<br class='hiddenLineBreak'>
			First, make sure you have
			<a
				href="https://svelte.dev/docs/introduction"
				class="hover:text-indigo-400 underline"
				target="_blank"
				title="Visit Svelte.dev for installation info">Svelte</a
			>,
			<a
				href="https://nodejs.org/en"
				class="hover:text-indigo-400 underline"
				target="_blank"
				title="Visit Nodejs.org for installation info">Node</a
			>, and
			<a
				href="https://tailwindcss.com/docs/installation"
				class="hover:text-indigo-400 underline"
				target="_blank"
				title="Visit tailwindcss.com for installation info">Tailwind CSS (optional)</a
			>
			installed. <br />
			Then, install SvARIA using the following command:
		</p>
	</h5>
	<div class="pt-4 rounded-lg leading-[21px] relative z-10 flex md:w-3/4 w-[85vw] text-black dark:text-white border border-black/[15%] ml-auto mr-auto dark:border-gray-650 bg-black dark:bg-gray-850">
		<code class="w-full grid h-9">
			<div class="flex flex-row justify-between px-4">
				<div>
					<span style="color: rgb(220, 220, 170);">npm</span>
					<span style="color: rgb(206, 145, 120);">install svaria-toolkit</span>
				</div>
				<button
					on:click={handleClick}
					id="clipBoardButton"
					class="flex flex-row rounded-md text-sm gap-2 text-black/75 hover:bg-black/[7.5%] hover:text-black dark:text-white/75 dark:hover:bg-white/5 dark:hover:text-white"
					type="button"
				>
					<span id="toolTip">copy to clipboard</span>
		
					<svg
						fill="none"
						viewBox="0 0 25 25"
						stroke="currentColor"
						stroke-width="1.5"
						class="h-5 w-5"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"
						>
						</path>
					</svg>
				</button>
			</div>
		</code>
	</div>
</div>