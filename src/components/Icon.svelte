<script>
  export let color;
  export let size = 32;
</script>

<div class="icon" style="--icon-color: {color}; --icon-size: {size}px;">
  <slot />
</div>

<style>
  .icon {
    display: inline-block;
    color: var(--icon-color, black);
    width: var(--icon-size);
    height: var(--icon-size);
  }
</style>