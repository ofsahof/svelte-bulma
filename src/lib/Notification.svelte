<script lang="ts">
  import type { TAccent } from "../types/index";

  export let type: TAccent = "";
  export let light = false;

  $: notificationType = () => {
    return `${type ? `is-${type}` : ""}`;
  };
</script>

<div class:is-light={light} class={`notification ${notificationType()}`}>
  <slot />
</div>
