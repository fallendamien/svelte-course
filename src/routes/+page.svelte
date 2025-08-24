<script lang="ts">
	import Button from '$lib/assets/components/Button.svelte';
	import { AlarmCheck, AlarmClock, Search } from '@lucide/svelte';
</script>

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
