<script>
  import { createEventDispatcher } from "svelte";
  import { slide } from "svelte/transition"
  const dispatch = createEventDispatcher();
    import { each } from "svelte/internal";

  export let contacts;

  const delContact = (id) => {
    dispatch("delContact", id);
  }
</script>

  {#each contacts as contact}
    <main transition:slide|local>
      <span class="image">{contact.name[0].toUpperCase()}</span>
      <span class="name">{contact.name}</span>
      <span class="email">{contact.email}</span>
      <span class="btnSection">
        <button on:click="{() => delContact(contact.id)}">Delete</button>
      </span>
    </main>
  {/each}

<style>
  main {
    width: 100%;
    padding: 8px 10px;
    background: #fff;
    border-radius: 3px;
    display: flex;
    height: 70px;
    align-items: center;
    justify-content: center;
    margin: 7px 0;
  }

  .image {
    display: inline-block;
    margin: 0 10px;
    width: 55px;
    height: 55px;
    background: linear-gradient(to right, #6547e3, skyblue);
    font-weight: bold;
    border-radius: 50%;
    box-shadow: 0 10px 20px rgba(0,0,0,0.2);
    line-height: 55px;
    text-align: center;
    color: #fff;
    font-size: 20px;
  }
  .name {
    display: inline-block;
    margin: 0 10px;
    width: 180px;
  }
  .email {
    display: inline-block;
    margin: 0 10px;
    width: 180px;
  }
  .btnSection {
    display: inline-block;
    margin: 0 10px;
  }
  button {
    border: none;
    padding: 10px 20px;
    border-radius: 3px;
    background: linear-gradient(to right, #e74c3c, #7a303a);
    color: #fff;
    outline: none;
    cursor: pointer;
    box-shadow: 0 10px 20px rgba(0,0,0,0.2);
  }
</style>