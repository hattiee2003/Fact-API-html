<script>
	let fact = ''
	
  async function getFacts() {
    let response = await fetch("https://harriet-facts.netlify.app/.netlify/functions/random-fact");
    response = await response.json();
  	fact = response.body
  }
</script>

<h1>Facts about me!!!!</h1>

<button on:click={getFacts}>
	Click to get a fact!
</button>

<p>
	{fact}
</p>
