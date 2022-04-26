<script>
	export let name;
	let result=0;
	let a=0;
	let b=0;

	function initRnNum() {
		console.log('just initialized')
		a = 0;
		b = 0;
		result = 0;
	}

	function myrandom(ary){
		initRnNum();
		console.log('inside myRandom');
		console.log('a =', a, ' b =', b, ' result =');
		a = Math.floor(Math.random() *100 + 1);
		b = Math.floor(Math.random() *100 + 1);
	}
	function myadd(ary){
		console.log('Inside myAdd');
		result = a+b;
	}
	initRnNum();
</script>

<main>
	<h1>Hello {name}!</h1>
	<p>Prior to generate Rn the values of {a} + {b} = {result}</p>
	<button on:click="{initRnNum}">ReInit</button>
	<button on:click={myrandom}>Generate Random Number</button>
	<button on:click={myadd}>sum</button>
	<p>sum of {a} + {b} = {result}</p>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: red;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>