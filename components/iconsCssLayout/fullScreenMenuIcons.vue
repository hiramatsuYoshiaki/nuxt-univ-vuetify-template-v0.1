<template lang="pug">
  div.content 
    div.fullScreenMenu
        div.menu 
          div.element-text70
          div.element-text30
          div.element-text50
          div.close-button
            div X
        
        
</template>

<style lang="scss" scoped>
// * {
//   border: 1px dotted grey;
// }
.content {
  position: relative;
  width: 100%;
  height: 100%;
  align-items: center;
  display: flex;
  justify-content: center;
  padding: 8px;
}
.fullScreenMenu {
  /* Full screen overlay */
  height: 100%;
  left: 0;
  // position: fixed;
  position: absolute;
  top: 0;
  width: 100%;
  /* Center the content */
  align-items: center;
  display: flex;
  justify-content: center;
}
.menu {
  position: relative;
  width: 100%;
  height: 100%;
  background-color: lightgrey;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.close-button {
  position: absolute;
  top: 4px;
  right: 4px;
  width: 16px;
  height: 16px;
  border-radius: 9999px;
  background-color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  color: black;
}
.element-text70 {
  width: 70%;
  height: 8px;
  background-color: rgba(0, 0, 0, 0.6);
  border-radius: 2px;
  margin: 2px;
}
.element-text50 {
  width: 50%;
  height: 8px;
  background-color: rgba(0, 0, 0, 0.6);
  border-radius: 2px;
  margin: 2px;
}
.element-text30 {
  width: 30%;
  height: 8px;
  background-color: rgba(0, 0, 0, 0.6);
  border-radius: 2px;
  margin: 2px;
}
</style>
