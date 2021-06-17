<script lang="ts">
  import type { TSize, TAccent } from "../types/index";
  export let type = "input";
  export let placeholder = "";
  export let style: TAccent = "";
  export let size: TSize = "";
  export let rounded = false;
  export let hovered = false;
  export let focused = false;
  export let classname = "";

  $: inputType = () => {
    return `${style ? `is-${style}` : ""}`;
  };

  $: inputSize = () => {
    return `${size ? `is-${size}` : ""}`;
  };
</script>

<input
  {type}
  {placeholder}
  class:is-rounded={rounded}
  class:is-focused={focused}
  class:is-hovered={hovered}
  on:keydown
  on:keypress
  on:keyup
  class={`${classname} input ${inputType()} ${inputSize()}`}
/>
