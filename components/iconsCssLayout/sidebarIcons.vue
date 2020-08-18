<template lang="pug">
  div.sidebar
    div.aside
        .element-text100
        .element-text100
        .element-text80
        .element-text60
    div.main
        
        .element-text100
        .element-text100
        .element-text100
        .element-text100
        .element-text80
        .element-text30
        .element-text30
        .element-text100
        .element-text80
        .element-text30
        .element-text100
        .element-text100
        .element-text80
        .element-text60
</template>

<style lang="scss" scoped>
.sidebar {
  display: flex;
  width: 100%;
  height: 100%;
  // border-right: 1px solid rgba(0, 0, 0, 0.3);
}
.aside {
  width: 30%;
  padding: 4px;
}
.main {
  /* Take the remaining width */
  flex: 1;

  /* Make it scrollable */
  overflow: auto;
  padding: 4px;
  border: 3px solid rgba(0, 0, 0, 0.3);
}

.element-text30 {
  width: 30%;
  height: 2px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  margin-bottom: 6px;
}
.element-text80 {
  width: 80%;
  height: 2px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  margin-bottom: 6px;
}
.element-text100 {
  width: 100;
  height: 2px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  margin-bottom: 6px;
}
</style>
