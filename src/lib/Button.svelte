<script lang="ts">
	// import type { ButtonType } from '../types.js';
	export let content: string = 'This is a button';
	export let ariaLabel: string = content;
	export let id: string = '';
	export let style: string = '';
	export let className: string = 'bg-black text-white text-bold hover:bg-gray-700 rounded py-2 px-4 rounded';
	export let type: ButtonType = 'button';
</script>

<button
	{id}
	aria-label={ariaLabel}
	class={className}
	on:click
	{style}
	{type}>{@html content}</button
>
