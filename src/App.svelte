<script>
  let fname = "jimmy";
  let sname = "hendrix";
  let ncolor = "gray";

  $: fullName = `${fname} ${sname}`;
</script>

<main>
  <h1 style="color:{ncolor}">Hello {fullName}!</h1>
  <input type="text" bind:value={fname} />
  <input type="text" bind:value={sname} />
  <input type="text" bind:value={ncolor} />
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
