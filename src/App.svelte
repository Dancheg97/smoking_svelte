<script>
  let name = "dancheg";
  let counter = 1;
  function increment() {
    counter += 1;
  }
  let color = "black";
</script>

<main>
  <h1 style="color: {color}">Hello {name}!</h1>
  <p>{counter}</p>
  <button on:click={increment}>Increment counter</button>
  <input type="text" bind:value={color} />
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
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
