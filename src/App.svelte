<script lang="ts">
let counter: number = 0;

const modifyCounter = (value: number) =>  counter += value ; 
const reset = () =>  counter = 0 ; 
/*
const add = (): number =>  counter += 1;

const diminidh = (): void => {
  counter -= 1;
};
const reset = (): void => {
  counter = 0;
};
*/
</script>

<main>
  <h1>Counter app </h1>
  <hr />

  <h2 class={counter < 0 ? "negative" : "positive" }>Count: {counter}</h2>

  <button class = "add" on:click={()=>modifyCounter(1)}>+1</button>
  <button class = "diminidh" on:click={()=>modifyCounter(-1)}>-1</button>
  <button class = "reset" on:click={reset}>0</button>
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
  h2 {
    font-style: italic;
    font-size: 2em;
  }
  .positive{
    color: olive;
  }
  .negative{
    color: crimson;
  }
  .add{
    background-color: greenyellow;
    color: white;
  }
  .add:active{
    background-color: darkgreen;
    color: white;
  }
  .diminidh{
    background-color: red;
    color: white;
  }
  .reset{
    background-color: blueviolet;
    color: white;
  }

  button{
    font-size: 1.5em;
    padding: 0.5em 1em;
    border: none;
    border-radius: 0.25em;
    margin: 0.5em;
    cursor: pointer;

  }
  button:hover{
   cursor : pointer
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
