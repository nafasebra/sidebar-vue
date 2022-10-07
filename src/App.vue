<script setup>

</script>

<template>
  <div class="items_center">
    <button class="button button_icon">
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
    background-color: black;
    width: 150px;
    height: 3px;
  }
  .button_icon span:first-child {
    transform: translateY(-50px);
  }
  .button_icon span:first-child {
    transform: translateY(50px);
  }
  .button_icon.active span:first-child {
    transform: rotate(-45deg)
  }
  .button_icon.active span:first-child {
    transform: rotate(45deg)
  }
</style>
