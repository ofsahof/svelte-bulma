<script lang="ts">
    import type { TSize } from "../types/index";
    export let size: TSize = "";
    export let classname = "";

    $: deleteSize = () => {
    return `${size ? `is-${size}` : ""}`;
  };
</script>

<button on:click class={`delete ${deleteSize()} ${classname}`} aria-label="delete"></button>