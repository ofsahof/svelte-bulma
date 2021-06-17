<script lang="ts">
    import type { TSize } from "../types/index";
    export let size: TSize = "";

    $: deleteSize = () => {
    return `${size ? `is-${size}` : ""}`;
  };
</script>

<button on:click class={`delete ${deleteSize()}`}></button>