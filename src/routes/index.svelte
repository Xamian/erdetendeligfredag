<script>
	let isFriday = new Date().getDay() === 5;
	let daysleft = 5 - new Date().getDay();
</script>

<h1>Er det endelig fredag?</h1>
{#if isFriday}
	<p>Ja, det er fredag!</p>
{:else}
	<p>Nej, det er ikke fredag, men der er kun {daysleft} dage til!</p>
{/if}
