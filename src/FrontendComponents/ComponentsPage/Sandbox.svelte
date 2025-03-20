<script lang='ts'>
	export let title: string = '';
	export let source: string = '';
	export let label: string = '';
</script>

<div class="flex flex-col w-full">
	<div id='sandboxOverlay' class="">
		<div class="flex w-full bg-[#2e2e2e] font-medium py-2 px-3 text-left text-3xl text-white rounded-t-xl">
			SvARIA {label} Component
		</div>
	</div>
	<iframe
		title={title}
		src={source}
		class="rounded-b-xl w-full h-[70vh]"
		id='sandbox'
	></iframe> 
</div>