<script>
	let firstName = $state('Zamri');
	let lastName = $state('Rosli');
	let fullName = $derived.by(() => {
		console.log('fullName derived');
		return `${firstName} ${lastName}`;
	});
	let username = $state('zamros');
	let src = 'https://picsum.photos/250/300';
	let bio = 'Hello, <b>this</b> is me.';

	$effect(() => {
		if (username || fullName) {
			console.log('User has a username or a full name.');
		}
	});
</script>

<button
	onclick={() => {
		console.log(fullName);
	}}>Get Full Name</button
>
<input bind:value={username} />
<input
	value={firstName}
	oninput={(e) => {
		firstName = e.currentTarget.value;
		fullName = 'Jong';
		console.log(fullName);
	}}
/>
<input bind:value={lastName} />
<!-- <img {src} alt="A photo of {name}" /> -->
<h1>{username || fullName}</h1>
<p>{@html bio}</p>

<style>
	h1 {
		color: red;
	}
</style>
