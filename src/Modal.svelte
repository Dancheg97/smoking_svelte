<script lang="ts">
  let show = true;
  function hide() {
    show = false;
  }
</script>

{#if show}
  <div class="backdrop">
    <div class="modal">
      <h3>Modal window!</h3>
      <p>Some dummy shit is listed over here... Just read :D</p>
      <button on:click={hide}> Hide </button>
    </div>
  </div>
{/if}

<style>
  .backdrop {
    width: 100%;
    height: 100%;
    position: fixed;
    background: rgba(0, 0, 0, 0.8);
  }
  .modal {
    padding: 10px;
    border-radius: 10px;
    max-width: 400px;
    margin: 10% auto;
    text-align: center;
    background: white;
  }
</style>
