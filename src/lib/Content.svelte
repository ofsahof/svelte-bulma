<script lang="ts">
    export let classname = "";
</script>

<div class={`content ${classname}`}>
    <slot />
</div>