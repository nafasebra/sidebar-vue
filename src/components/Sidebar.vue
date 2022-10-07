<script>
export default {
  props: {
    opened: Boolean,
  },
};
</script>

<template>
  <aside class="sidebar_container" :class="opened && 'active'">
    <ul class="menu-list">
      <li><a>Dashboard</a></li>
      <li><a>Customers</a></li>
    </ul>
    <p class="menu-label">Administration</p>
    <ul class="menu-list">
      <li><a>Team Settings</a></li>
      <li>
        <a class="is-active">Manage Your Team</a>
        <ul>
          <li><a>Members</a></li>
          <li><a>Plugins</a></li>
          <li><a>Add a member</a></li>
        </ul>
      </li>
      <li><a>Invitations</a></li>
      <li><a>Cloud Storage Environment Settings</a></li>
      <li><a>Authentication</a></li>
    </ul>
    <p class="menu-label">Transactions</p>
    <ul class="menu-list">
      <li><a>Payments</a></li>
      <li><a>Transfers</a></li>
      <li><a>Balance</a></li>
    </ul>
  </aside>
</template>

<style scoped>
.sidebar_container {
  position: fixed;
  top: 0;
  left: 0;
  bottom: 0;
  transform: translateX(-300px);
  width: 250px;
  visibility: hidden;
  opacity: 0;
}
.sidebar_container.active {
  transform: translateX(0);
  opacity: 1;
  visibility: visible;
}
</style>
