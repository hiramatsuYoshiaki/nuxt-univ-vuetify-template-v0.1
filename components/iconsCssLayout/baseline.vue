<template lang="pug">
  div.holyGrail
    div.header 
      div.app-bar v-app-bar 
    div.main 
      div.aside 
        div.navigation-drawer v-navigation-wrawer
      div.article 
       div container
    div.footer 
      div.footer-bar v-footer
</template>

<style lang="scss" scoped>
// * {
//   border: 1px solid rgba(0, 0, 0, 0.3);
// }
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

.navigation-drawer {
  width: 100%;
  line-height: 8px;
  color: grey;
  word-wrap: wrape;
}
.main {
  // Take the remaining height
  flex-grow: 1;
  // Layout the left sidebar, main content and right sidebar
  display: flex;
  flex-direction: row;
}
// Left sidebar
.aside {
  width: 30%;
  padding: 4px;
  border-right: 1px solid rgba(0, 0, 0, 0.3);
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

// .element-text100 {
//   width: 100%;
//   height: 8px;
//   background-color: rgba(0, 0, 0, 0.3);
//   border-radius: 10px;
//   margin-bottom: 2px;
// }
// .element-text60 {
//   width: 60%;
//   height: 2px;
//   background-color: rgba(0, 0, 0, 0.3);
//   border-radius: 10px;
//   margin-bottom: 2px;
// }
// .element-title60 {
//   width: 60%;
//   height: 4px;
//   background-color: rgba(0, 0, 0, 0.3);
//   border-radius: 10px;
//   margin-bottom: 2px;
// }
</style>
