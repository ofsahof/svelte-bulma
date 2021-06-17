<script lang="ts">
    export let classname;
</script>

<div class={`box ${classname}`}>
    <slot />
</div>