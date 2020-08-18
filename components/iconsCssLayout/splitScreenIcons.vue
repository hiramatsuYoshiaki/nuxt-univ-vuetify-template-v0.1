<template lang="pug">
    div.splitScreen
        div.content-left
            div.circle
        div.content-right 
            div.element-text100
            div.element-text80
            div.element-text30
</template>

<style lang="scss" scoped>
.splitScreen {
  display: flex;
  width: 100%;
  height: 100%;
}
.content-left {
  flex: 1;
  height: 100%;
  padding: 4px;
  border-right: 1px solid rgba(0, 0, 0, 0.3);
  display: flex;
  justify-content: center;
  align-items: center;
}
.content-right {
  flex: 1;
  height: 100%;
  padding: 4px;
}
.circle {
  width: 20px;
  height: 20px;
  border-radius: 9999px;
  background-color: rgba(0, 0, 0, 0.3);
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
