<script lang="ts">
	import Button from '$lib/assets/components/Button.svelte';
	import { AlarmCheck, AlarmClock, Search } from '@lucide/svelte';
</script>

<Button size="sm" shadow>
	{#snippet left(isHovered)}
		{#if isHovered}
			<Search />
		{:else}
			<AlarmCheck />
		{/if}
	{/snippet}

	{#snippet children(isLeftHovered)}
		Text {isLeftHovered}
	{/snippet}

	{#snippet right()}
		<AlarmCheck />
	{/snippet}
</Button>
