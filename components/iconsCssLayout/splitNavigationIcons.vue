<template lang="pug">
    div.splitNavigation 
        ul 
            li 
                nuxt-link(:to="'/cssLayout'")
                    div.element-text15
            li
                nuxt-link(:to="'/cssLayout'")
                    div.element-text15
            li.sticks-right
                nuxt-link(:to="'/cssLayout'")
                    div.element-text15
</template>

<style lang="scss" scoped>
.splitNavigation {
  /* Content is centered vertically */
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
  padding: 8px;
}
ul {
  /* Content is centered horizontally */
  align-items: center;
  display: flex;

  /* Reset styles */
  list-style-type: none;
  margin: 0;
  width: 100%;
  border: 1px solid rgba(0, 0, 0, 0.3);
  padding: 2px;
}
.sticks-right {
  /* Sticks to the right */
  margin-left: auto;
}
.element-text15 {
  display: inline-block;
  width: 15px;
  height: 8px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 2px;
  margin: 2px 2px 4px 2px;
  vertical-align: bottom;
}
a {
  &:hover {
    opacity: 0.5;
  }
}
</style>
