<script lang="ts">
	import Button from '$lib/assets/components/Button.svelte';
	import { AlarmCheck, AlarmClock, Search } from '@lucide/svelte';
	let html = '<p>adfbssdgs</p>';
</script>

<div class="wrapper">
	{@html html}
	<Button size="sm" class={{ test: true }} shadow bgColor="green" textColor="yellow">
		{#snippet left(isHovered)}
			{#if isHovered}
				<Search />
			{:else}
				<AlarmCheck />
			{/if}
		{/snippet}

		{#snippet content(isLeftHovered)}
			Text {isLeftHovered}
		{/snippet}

		{#snippet right()}
			<AlarmCheck />
		{/snippet}
	</Button>
</div>

<style>
	/* :global(body) {
		background-color: #222;
	} */
	:global {
		body {
			background-color: #222;
		}
		.wrapper p {
			color: white;
		}
	}

	/* @keyframes --global-move {
	} */

	/* .wrapper :global(button) {
		background-color: blue !important;
	} */
	.wrapper :global {
		button {
			background-color: blue !important;
		}
	}
</style>
