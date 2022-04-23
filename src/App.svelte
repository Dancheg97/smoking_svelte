<script>
  let people = [
    { fname: "tasty", sname: "sweety", age: 21, iq: 128 },
    { fname: "cobol", sname: "krik", age: 23, iq: 122 },
    { fname: "upper", sname: "obal", age: 34, iq: 110 },
    { fname: "uner", sname: "pjer", age: 34, iq: 110 },
  ];
</script>

<main>
  {#each people as person}
    <h1 style="color:{person.fname}">
      Hello {person.sname}! He's {person.age}
    </h1>
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
