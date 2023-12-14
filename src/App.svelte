<script lang="ts">
  let counter: number = 0;

  const modifyCounter = (value: number): number=> counter += value;

  const rest = ()=>{counter=0}

  //const add = ():number => counter++;
  //const rest = (): number => counter = counter - 1;

  //const reset = (): void => {counter = 0};
  
</script>

<main>
  <h1>Hello Word - {new Date()}</h1>
  <h2 class={counter < 0 ? "negative" : "positive"}>counter : {counter}</h2>

  <button class="add" on:click={()=>modifyCounter(1)}>Suma +1</button>
  <button class="diminish" on:click={()=>modifyCounter(-1)}>Resta -1</button>
  <button class="reset" on:click={rest}>Reset </button>
</main>

<style>
  button:hover {
    cursor: pointer;
  }
  button {
    font-size: 2rem;
    font-family: console;
    margin: 2px;
    border-radius: 5px;
  }

  .add {
    background-color: #f3b50c;
  }

  .add:active {
    background-color: #26d231;
  }

  .diminish {
    background-color: aqua;
  }

  .diminish:active {
    background-color: rgb(161, 240, 16);
  }

  .reset {
    background-color: burlywood;
  }
  .reset:active {
    background-color: rgb(216, 27, 43);
  }

  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: rgb(63, 60, 59);
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }
  h2 {
    font-size: 20 rem;
  }

  .positive {
    color: olivedrab;
  }

  .negative {
    color: #f3b50c;
  }
  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
