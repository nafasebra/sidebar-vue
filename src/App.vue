<script>
export default {
  data() {
    return {
      showSidebar: false
    }
  },
  methods: {
    setShow() {
      this.showSidebar = !this.showSidebar;
    }
  }
}
</script>

<template>
  <div class="items_center">
    <button @click="setShow" class="button_icon" :class="showSidebar && 'active'">
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
    justify-content: center;
    align-content: center;
    height: 100px;
    border: none;
    outline: none;
    background: transparent;
    cursor: pointer;
  }
  .button_icon span {
    display: block;
    background-color: black;
    width: 100px;
    height: 3px;
  }
  .button_icon span:first-child {
    transform: translateY(-25px);
  }
  .button_icon span:last-child {
    transform: translateY(25px);
  }
  .button_icon.active span:first-child {
    transform: rotate(-45deg)
  }
  .button_icon.active span:last-child {
    transform: rotate(45deg)
  }
</style>
