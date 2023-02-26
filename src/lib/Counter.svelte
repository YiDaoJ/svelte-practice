<script lang="ts">
  let counter: number = 0;

  let output: string;
  // reactive statement
  // $: if(counter > 5) {
  //   output = `you have clicked ${counter} times.`;
  // }
  $: output = `you have clicked ${counter} times.`;

  const increase = () => {
    counter += 1;
  };
</script>

<button on:click={increase}> click </button>
<div>
  Counter: {counter}
</div>
<div>{output}</div>

<style>
  button {
    padding: 1rem 1.5rem;
    font-size: 1.5rem;
  }
</style>
