<script setup>

</script>

<template>
  <div class="items_center">
    <button class="button_icon">
      <span></span>
      <span></span>
    </button>
  </div>
</template>

<style scoped>
  .items_center {
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
  }
  .button_icon {
    display: flex;
    flex-direction: column;
  }
  .button_icon span {
    display: block;
  }
</style>
