<template lang="pug">
    div.nestedDropdowns
        ul.p-nested-dropdowns
            li.item-left.dropdown  
                div.circle 
                  ul.dropdown-nest   
                    li 
                        div.element-text20 
                    li 
                        div.element-text10 
                    ul.dropdown-child 
                      li 
                          div.element-text10 
                      li 
                          div.element-text20 
                   
            li.item
                div.circle
                    
            li.item-right 
                div.circle 
</template>

<style lang="scss" scoped>
.nestedDropdowns {
  /* Content is centered vertically */
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
  padding: 8px;
}
.p-nested-dropdowns {
  display: flex;
  /* Reset list styles */
  list-style-type: none;
  margin: 0;
  padding: 0;
}
.p-nested-dropdowns li {
  /* Used to position the sub dropdown */
  position: relative;
}
/* The sub dropdown */
.p-nested-dropdowns ul.dropdown-nest {
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
  width: 30px;
  padding: 2px;
}
.p-nested-dropdowns ul.dropdown-child {
  /* Border */
  border: 1px solid rgba(0, 0, 0, 0.3);

  /* Hidden by default */
  display: none;

  /* Absolute position */
  left: 30px;
  position: absolute;
  top: 50%;

  /* Reset styles */
  list-style-type: none;
  margin: 0;
  padding: 0;

  /* Width */
  width: 30px;
  padding: 2px;
}
.dropdown {
  &:hover {
    ul.dropdown-nest {
      display: block;
    }
  }
}
.dropdown-nest {
  &:hover {
    ul.dropdown-child {
      display: block;
    }
  }
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

.element-text20 {
  width: 20px;
  height: 2px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  margin: 2px;
}
.element-text10 {
  width: 10px;
  height: 2px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  margin: 2px;
}
</style>
