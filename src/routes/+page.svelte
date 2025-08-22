<script lang="ts">
	import Button from '$lib/assets/components/Button.svelte';
	import { AlarmCheck, AlarmClock, Search } from '@lucide/svelte';
</script>

<Button>
	{#snippet left(isHovered: boolean)}
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
