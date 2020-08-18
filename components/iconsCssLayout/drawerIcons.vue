<template lang="pug">
    div.drawer 
        div.backdrop
        div.sidebar.action
            div.element-text100
            div.element-text100
            div.element-text100
            div.element-text60
</template>

<style lang="scss" scoped>
.drawer {
  position: relative;
  width: 100%;
  height: 100%;
}
.backdrop {
  //   position: relative;
  position: absolute;
  z-index: -1;
  background-color: rgba(0, 0, 0, 0.5);
  width: 100%;
  height: 100%;
}
.sidebar {
  position: absolute;
  background-color: rgba(250, 250, 250, 1);
  width: 100%;
  height: 100%;
  padding: 4px;
  transform: translateX(-80px);
  transition: 0.5s;
}
.action {
  &:hover {
    transform: translateX(0);
    transition: 0.5s;
  }
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
</style>
