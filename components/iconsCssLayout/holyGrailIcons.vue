<template lang="pug">
  div.holyGrail
    div.header 
      div.element-title60
      
    div.main 
      div.aside 
        div.element-text100 
        div.element-text60 
        
      
      div.article 
       div.element-text100 
       div.element-text60
       div.element-text100 
       div.element-text60
       
      div.nav 
        div.element-text100 
        div.element-text60
    div.footer 
      div.element-title60

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
  border-bottom: 1px solid rgba(0, 0, 0, 0.3);
}
.element60 {
  width: 60%;
  height: 4px;
  background-color: rgba(0, 0, 0, 0.5);
  // border-radius: 10px;
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
  width: 25%;
  padding: 4px;
  border-right: 1px solid rgba(0, 0, 0, 0.3);
}
// Main content
.article {
  /* Take the remaining width */
  flex-grow: 1;
  padding: 4px;
  border-right: 1px solid rgba(0, 0, 0, 0.3);
}
.nav {
  width: 20%;
  padding: 4px;
}
.footer {
  border-top: 1px solid rgba(0, 0, 0, 0.3);
  padding: 4px;
}

.element-text100 {
  width: 100%;
  height: 2px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  margin-bottom: 2px;
}
.element-text60 {
  width: 60%;
  height: 2px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  margin-bottom: 2px;
}
.element-title60 {
  width: 60%;
  height: 4px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  margin-bottom: 2px;
}
</style>
