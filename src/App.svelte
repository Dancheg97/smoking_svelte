<script>
  let name = "dancheg";
  let counter = 1;
  function increment() {
    counter += 1;
  }
</script>

<main>
  <h1>Hello {name}!</h1>
  <p>{counter}</p>
  <button on:click={increment}>update some stuff</button>
  <input type="text" bind:value={name} />
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
