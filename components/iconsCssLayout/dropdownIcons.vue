<template lang="pug">
    div.dropdown
      div.dropdown-button.dropdown-action  
        div &or;
        div.dropdown-items 
          div.item.item-border-bottom 
            div.element-text100
          div.item.item-border-bottom 
            div.element-text50
          div.item 
            div.element-text30
          //- div.item 
          //-   div.element-text100
          //- div.item 
          //-   div.element-text100
</template>

<style lang="scss" scoped>
.dropdown {
  position: relative;
  padding: 8px;
}
.dropdown-button {
  position: relative;
  width: 40px;
  height: 20px;
  border: 1px solid rgba(0, 0, 0, 0.5);
  border-radius: 4px;
  padding: 2px;
  text-align: right;
  margin-bottom: 2px;
  transition: opacity 0.5s;
}
.dropdown-action {
  &:hover {
    .dropdown-items {
      // display: block;
      opacity: 1;
    }
  }
}
.dropdown-items {
  position: absolute;
  top: 0;
  left: 0;
  width: 80px;
  margin-top: 22px;
  display: block;
  border: 1px solid rgba(0, 0, 0, 0.5);
  border-radius: 4px;
  // display: none;
  opacity: 0.3;
}
.item {
  padding: 4px;
}
.item-border-bottom {
  border-bottom: 1px solid rgba(0, 0, 0, 0.3);
}
.element-text100 {
  width: 100%;
  height: 2px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  margin: 2px;
}
.element-text50 {
  width: 50%;
  height: 2px;
  background-color: rgba(0, 0, 0, 0.3);
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
