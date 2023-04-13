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
	const daysleft = (days.friday - today + 7) % 7;
</script>

{@debug isFriday, daysleft}

<title>Beer day?</title>

<h1>Er det endelig fredag?</h1>
{#if isFriday}
	<p>Ja, det er fredag!</p>
{:else}
	<p>Nej, det er ikke fredag, men der er kun {daysleft} {daysleft > 1 ? 'dage' : 'dag'} til!</p>
{/if}

<footer>
	<p><a href="https://max-it.dk">max-it.dk</a> &copy; 2022</p>
	<p>
		Highly advanced <a href="https://github.com/xamian/erdetendeligfredag">code</a> that can figure out
		if it is indeed friday.
	</p>
</footer>
