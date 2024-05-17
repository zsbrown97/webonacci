<script lang="ts">
  let length: number = 5
  let name: string = 'Zack';

  function displaySequence(length: number) {
    const result: Array<number> = [1, 1]

    for (let i = 2; i < length; i++) {
      result[i] = result[i - 1] + result[i - 2];
    }
    return result;
  }
</script>

<div>
  <h2>What is your name?</h2>
  <input type="string" bind:value={name} />
  <h1>Hello, {name}</h1>
</div>
<input type="number" bind:value={length} />

<p>{length} numbers of the fibonacci sequence: </p>
<h3>{displaySequence(length).join(', ')}</h3>
