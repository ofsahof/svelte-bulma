<script lang="ts">
  import Button from "./lib/Button.svelte";
  import Box from "./lib/Box.svelte";
  import Delete from "./lib/Delete.svelte";
</script>

<div class="block">
  <span class="tag is-success">
    Hello World
    <Delete size="small"></Delete>
  </span>
</div>

<div class="notification is-danger">
  <Delete></Delete>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit lorem ipsum dolor sit amet, consectetur adipiscing elit
</div>

<article class="message is-info">
  <div class="message-header">
    Info
    <Delete></Delete>
  </div>
  <div class="message-body">
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque risus mi, tempus quis placerat ut, porta nec nulla. Vestibulum rhoncus ac ex sit amet fringilla. Nullam gravida purus diam, et dictum felis venenatis efficitur. Aenean ac eleifend lacus, in mollis lectus. Donec sodales, arcu et sollicitudin porttitor, tortor urna tempor ligula, id porttitor mi magna a neque. Donec dui urna, vehicula et sem eget, facilisis sodales sem.
  </div>
</article>