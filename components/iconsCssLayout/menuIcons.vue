<template lang="pug">
    div.menu
        div.menu-items 
          div.item.item-border-bottom 
            div.element-text100
          div.item.item-border-bottom 
            div.element-text50
          div.item 
            div.element-text30
         
</template>

<style lang="scss" scoped>
.menu {
  position: relative;
  padding: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
}

.menu-items {
  width: 100%;
  display: block;
  border: 1px solid rgba(0, 0, 0, 0.5);
  border-radius: 4px;
}
.item {
  padding: 4px;
}
.item-border-bottom {
  border-bottom: 1px solid rgba(0, 0, 0, 0.5);
}
.element-text100 {
  width: 100%;
  height: 2px;
  background-color: rgba(0, 0, 0, 0.5);
  border-radius: 10px;
  margin: 2px;
}
.element-text50 {
  width: 50%;
  height: 2px;
  background-color: rgba(0, 0, 0, 0.5);
  border-radius: 10px;
  margin: 2px;
}
.element-text30 {
  width: 30%;
  height: 2px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  margin: 2px;
}
</style>
