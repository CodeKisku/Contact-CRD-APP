<script>
  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();
  import { v4 as uuidv4 } from 'uuid';

  export let modelStatus;
  let name;
  let email;
  const updateModel = () => {
    dispatch("updateModel")
  }

  const addContact = (e) => {
    // e.preventDefault();
    const id = uuidv4();
    dispatch("addContact", {id, name, email});
    name = "";
    email = "";
  }
</script>

{#if modelStatus}
<!-- svelte-ignore a11y-click-events-have-key-events -->
<main on:click|self={updateModel}>
  <form on:submit|preventDefault={addContact}>
    <div class="group">
      <label for="name">Name</label>
      <input type="text" class="control" id="name" placeholder="Name" bind:value={name} required>
    </div>
    <div class="group">
      <label for="email">Email</label>
      <input type="email" class="control" id="email" placeholder="Email" bind:value={email} required>
    </div>
    <div class="group">
      <input type="submit" class="btn-block" value="Add Contact">
    </div>
  </form>
</main>
{/if}

<style>
  main {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0,0,0,.5);
    display: flex;
    align-items: center;
    justify-content: center;
  }

  form {
    width: 400px;
    height: 250px;
    background: #fff;
    border-radius: 3px;
    padding: 25px;
  }

  .group {
    margin: 7px 0;
  }

  label {
    font-weight: bold;
    color: silver;
    margin-bottom: 7px;
  }

  .control {
    width: 100%;
    padding: 10px 8px;
    border: none;
    background: #edf2f7;
    border-radius: 3px;
    outline: none;
  }

  .btn-block {
    border: none;
    padding: 10px 20px;
    border-radius: 3px;
    background: linear-gradient(to right, #6547e3, skyblue);
    color: #fff;
    outline: none;
    cursor: pointer;
    box-shadow: 0 10px 20px rgba(0,0,0,0.2);
    width: 100%;
    text-transform: uppercase;
  }
</style>