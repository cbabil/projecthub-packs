<script lang="ts">
  let count = $state(0);

  function increment() {
    count += 1;
  }
</script>

<button onclick={increment}>
  Count is {count}
</button>

<style>
  button {
    font-family: inherit;
    font-size: inherit;
    padding: 1em 2em;
    color: #ff3e00;
    background-color: rgba(255, 62, 0, 0.1);
    border-radius: 2em;
    border: 2px solid #ff3e00;
    cursor: pointer;
  }

  button:hover {
    background-color: rgba(255, 62, 0, 0.2);
  }
</style>
