<script lang="ts">
  import type { TAccent, TSize } from "../types/index";
  export let color: TAccent = "";
  export let size: TSize = "";

  $: messageColor = () => {
    return `${color ? `is-${color}` : ""}`;
  };

  $: messageSize = () => {
    return `${size ? `is-${size}` : ""}`;
  };
</script>

<article class={`message ${messageColor()} ${messageSize()}`}>
  {#if $$slots.messageHeader}
    <div class="message-header">
      <slot name="messageHeader" />
    </div>
  {/if}

  {#if $$slots.messageBody}
    <div class="message-body">
      <slot name="messageBody" />
    </div>
  {/if}
</article>
