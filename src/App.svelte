<script>
  export let name;
  let vip = '';
  let count = 0;

  $: reactiveCount = `FUCK ${count * 100} COUNT(s)`;

  function increment() {
    count++;
  }

  function decrement() {
    count--;
  }
</script>

<main>
	<h1>Hello {name}! a.k.a [{vip}]</h1>
  <div>
    <h3>counter: {count}</h3>
    <h3>computed counter: {reactiveCount}</h3>
    <button on:click="{increment}">+</button>
    <button on:click="{decrement}">-</button>
  </div>

  <div>
    <input type="text" bind:value="{vip}">
  </div>

</main>

<style>
</style>
