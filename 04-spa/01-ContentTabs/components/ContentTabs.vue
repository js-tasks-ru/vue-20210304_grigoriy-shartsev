<template>
  <div class="content-tabs">
    <div class="content-tabs__nav">
      <a href="#" class="content-tabs__tab">Page A</a>
      <a href="#" class="content-tabs__tab">Page B</a>
    </div>
    <div class="content-tabs__content">View Content From Slot</div>
  </div>
</template>

<script>
export default {
  name: 'ContentTabs',
};
</script>

<style scoped>
.content-tabs {
  margin: 0;
}

.content-tabs__content {
}

.content-tabs__nav {
  display: flex;
  flex-direction: row;
  position: relative;
}

.content-tabs__nav:before {
  content: '';
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 2px;
  background-color: var(--grey-2);
}

.content-tabs__tab {
  display: inline-flex;
  padding: 10px 0;
  font-weight: 400;
  font-size: 18px;
  text-decoration: none;
  line-height: 28px;
  color: var(--grey-8);
  border-bottom: 2px solid transparent;
  cursor: pointer;
  margin-right: 18px;
  transition: 0.2s all;
  box-shadow: none;
  background-color: transparent;
  outline: none;
  position: relative;
  z-index: 1;
}

.content-tabs__tab:hover,
.content-tabs__tab.content-tabs__tab_active {
  border-bottom-color: var(--blue);
  color: var(--blue);
}
</style>
