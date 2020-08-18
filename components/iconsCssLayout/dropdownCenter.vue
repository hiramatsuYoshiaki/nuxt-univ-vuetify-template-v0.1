<template lang="pug">
  div.holyGrail
    div.header 
      div.app-bar v-app-bar dropdown
    div.main 
      div.article 
       div container
      div.menus v-scroll-y-transition
    div.footer 
      div.footer-bar v-footer
</template>

<style lang="scss" scoped>
.holyGrail {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 100%;
}
.header {
  text-align: center;
  padding: 4px;
  border-bottom: 1px solid rgba(7, 4, 4, 0.3);
}
.app-bar {
  width: 100%;
  line-height: 16px;
  color: grey;
}

.footer-bar {
  width: 100%;
  line-height: 8px;
  color: grey;
}

.main {
  // Take the remaining height
  flex-grow: 1;
  // Layout the left sidebar, main content and right sidebar
  display: flex;
  flex-direction: row;
  position: relative;
  .menus {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    line-height: 32px;
    color: white;
    display: block;
    background-color: rgba(7, 4, 4, 0.5);
    padding-left: 4px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  &:hover {
    .menus {
      display: none;
      color: white;
    }
  }
}

// Main content
.article {
  /* Take the remaining width */
  flex-grow: 1;
  padding: 4px;
  //   border-right: 1px solid rgba(0, 0, 0, 0.3);
  display: flex;
  justify-content: center;
  align-items: center;
  color: grey;
}

.footer {
  border-top: 1px solid rgba(0, 0, 0, 0.3);
  padding: 4px;
  text-align: center;
}
</style>
