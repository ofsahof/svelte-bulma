<script lang="ts">
  import Button from "./lib/Button.svelte";
  import Box from "./lib/Box.svelte";
  import Delete from "./lib/Delete.svelte";
  import Input from "./lib/Input.svelte";
  import Message from "./lib/Message.svelte";
</script>

<Message color="danger" size="large">
  <svelte:fragment slot="messageHeader">
    <p slot="messageHeader">Warning</p>
    <Delete slot="messageHeader"></Delete>
  </svelte:fragment>

  <svelte:fragment slot="messageBody">
    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Fuga odio necessitatibus ipsa repellat autem repellendus, quam nam deserunt id a sit laborum et quia vero nulla, dolor tempora ducimus quod?
  </svelte:fragment>
</Message>
