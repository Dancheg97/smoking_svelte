<script>
  let people = [
    { fname: "tasty", sname: "sweety", age: 21, id: 1 },
    { fname: "cobol", sname: "krik", age: 23, id: 2 },
    { fname: "upper", sname: "obal", age: 34, id: 3 },
    { fname: "uner", sname: "pjer", age: 34, id: 4 },
  ];
</script>

<main>
  {#each people as person}
    <h1>
      Hello {person.sname}! He's {person.age}
    </h1>
    <button
      on:click={(event) => {
        console.log(event);
        people = people.filter((pers) => pers.id != person.id);
      }}
    >
      delete
    </button>
  {:else}
    <h1>No stuff buddy! :D</h1>
  {/each}
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
