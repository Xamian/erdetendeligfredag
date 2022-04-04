<script lang="ts">
	enum days {
		monday = 1,
		tuesday,
		wednesday,
		thursday,
		friday,
		saturday,
		sunday
	}
	const today = new Date().getDay();
	const isFriday = today === days.friday;
	const daysleft = days.friday - today;
</script>

{@debug isFriday, daysleft}

<h1>Er det endelig fredag?</h1>
{#if isFriday}
	<p>Ja, det er fredag!</p>
{:else}
	<p>Nej, det er ikke fredag, men der er kun {daysleft} dage til!</p>
{/if}
