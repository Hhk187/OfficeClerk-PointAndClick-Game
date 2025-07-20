<script>
  export let top = '50%';
  export let left = '50%';
  export let onStart = () => {};
</script>

<button class="start-btn" on:click={onStart}
  style="top: {top}; left: {left}; transform: translate(-50%, -50%);">
  START
</button>


<style>
  .start-btn {
    position: absolute;
    left: 69%;
    top: 70%;
    transform: translate(-50%, -50%);
    z-index: 10;
    font-size: 30px;
    background: #ff6cd1;
    border: none;
    border-radius: 30px;
    cursor: pointer;
    color: black;
    font-weight: bold;
    padding: 20px 30px;
    transition: background 0.3s ease, padding 0.3s ease;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    outline: none;
  }

  .start-btn:hover {
    background: #ff4bb0;
    padding: 25px 38px;
    transition: background 0.3s ease, padding 0.3s ease;
  }
  .start-btn:active {
    background: #ff2a8f;
    padding: 30px 42px;
    transition: background 0.3s ease, padding 2s ease;
  }
</style>
