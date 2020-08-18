<template lang="pug">
    div.megaMenu
        ul.p-mega-dropdowns
            li.item-left 
                div.circle.dropdown
                    ul.mega-menu
                        li 
                            div.element-text40 
                        li 
                            div.element-text60 
                        li 
                            div.element-text30 

            li.item.dropdown 
                div.circle
                    ul.mega-menu 
                        li 
                            div.element-text30 
                        li 
                            div.element-text40 
                        li 
                            div.element-text60 
            li.item-right 
                div.circle.dropdown 
                    ul.mega-menu
                        li 
                            div.element-text60
                        li 
                            div.element-text30 
                        li 
                            div.element-text30
                        li 
                            div.element-text30
                            
</template>

<style lang="scss" scoped>
.megaMenu {
  /* Content is centered vertically */
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
  padding: 8px;
}
.p-mega-dropdowns {
  display: flex;
  /* Reset list styles */
  list-style-type: none;
  margin: 0;
  padding: 0;
  position: absolute;
}

/* The sub dropdown */
.p-mega-dropdowns ul {
  /* Border */
  border: 1px solid rgba(0, 0, 0, 0.3);

  /* Hidden by default */
  display: none;

  /* Absolute position */
  left: 0;
  position: absolute;
  top: 100%;

  /* Reset styles */
  list-style-type: none;
  margin: 0;
  padding: 0;

  /* Width */
  width: 100%;
  padding: 2px;
}
.dropdown {
  &:hover {
    ul {
      display: block;
    }
  }
}
.mega-menu {
  position: absolute;
  top: 0;
  left: 0;
  width: 100px;
  border: 1px solid red;
}
.item {
  border: 1px solid rgba(0, 0, 0, 0.3);
  &:hover {
    background-color: rgba(0, 0, 0, 0.1);
  }
}
.item-left {
  border-left: 1px solid rgba(0, 0, 0, 0.3);
  border-top: 1px solid rgba(0, 0, 0, 0.3);
  border-bottom: 1px solid rgba(0, 0, 0, 0.3);
  &:hover {
    background-color: rgba(0, 0, 0, 0.1);
  }
}
.item-right {
  border-right: 1px solid rgba(0, 0, 0, 0.3);
  border-top: 1px solid rgba(0, 0, 0, 0.3);
  border-bottom: 1px solid rgba(0, 0, 0, 0.3);
  &:hover {
    background-color: rgba(0, 0, 0, 0.1);
  }
}
.circle {
  /* Rounded border */
  border-radius: 9999px;
  height: 10px;
  width: 10px;
  /* OPTIONAL: Spacing between circle */
  margin: 6px;
  background-color: rgba(0, 0, 0, 0.3);
}

.element-text40 {
  width: 40px;
  height: 2px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  margin: 2px;
}
.element-text60 {
  width: 60px;
  height: 2px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  margin: 2px;
}
.element-text30 {
  width: 30px;
  height: 2px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  margin: 2px;
}
</style>
