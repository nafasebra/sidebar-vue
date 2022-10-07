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
      <span></span>
    </button>
  </div>
  <Sidebar :opened="showSidebar" />
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
    overflow: hidden;
  }
  .button_icon span {
    display: block;
    background-color: black;
    width: 100px;
    height: 4px;
  }
  .button_icon span:first-child {
    transform: translateY(-25px);
  }
  .button_icon span:last-child {
    transform: translateY(25px);
  }
  .button_icon.active span:first-child {
    transform: rotate(-45deg) translateY(5.5px)
  }
  .button_icon.active span:nth-child(2) {
    transform: translateX(100%);
    opacity: 0;
  }
  .button_icon.active span:last-child {
    transform: rotate(45deg) translateY(-5.5px)
  }
</style>
