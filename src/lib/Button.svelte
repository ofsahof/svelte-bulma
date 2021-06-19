<script lang="ts">
  import type { TAccent, TSize } from "../types/index";

  export let classname = "";
  export let type: TAccent = "";
  export let size: TSize = "";
  export let outlined = false;
  export let loading = false;
  export let disabled = false;
  export let text = "";
  export let light = false;
  export let fullwidth = false;
  export let inverted = false;
  export let rounded = false;

  $: buttonType = () => {
    return `${type ? `is-${type}` : ""}`;
  };

  $: buttonSize = () => {
    return `${size ? `is-${size}` : ""}`;
  };
</script>

<button on:click
  {disabled}
  class:is-loading={loading}
  class:is-rounded={rounded}
  class:is-outlined={outlined}
  class:is-light={light}
  class:is-fullwidth={fullwidth}
  class:is-inverted={inverted}
  class={`
  button
  ${classname}
  ${buttonSize()}
  ${buttonType()}
  `}
>
  {#if $$slots.default}
    <slot />
  {:else}
    {text}
  {/if}
</button>
