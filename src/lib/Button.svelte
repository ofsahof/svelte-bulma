<script lang="ts">
  import type { TAccent, TSize } from "../types/index";

  export let className: string = "";
  export let type: TAccent = "";
  export let size: TSize = "";
  export let outlined = false;
  export let loading = false;
  export let disabled = false;
  export let text = "";
  export let light = false;

  $: buttonType = () => {
    return `${type ? `is-${type}` : ""}`;
  };

  $: buttonSize = () => {
    return `${size ? `is-${size}` : ""}`;
  };
</script>

<button
  {disabled}
  class:is-loading={loading}
  class:is-outlined={outlined}
  class:is-light={light}
  class={`
  button
  ${className}
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
