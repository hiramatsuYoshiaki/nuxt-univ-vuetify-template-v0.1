<template lang="pug">
    div.stickyHeader 
        div.header 
            div.element-text30 
        div.main 
            div.element-text100
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
        //- メインコンテンツをスクロールして、ヘッダーがページの上部に貼り付けられていることを確認してください。
</template>

<style lang="scss" scoped>
.stickyHeader {
  width: 100%;
  height: 100%;
  overflow: scroll;
}
.header {
  /* Stick to the top */
  position: sticky;
  top: 0;
  border-bottom: 1px solid rgba(0, 0, 0, 0.3);
  background-color: lightgrey;
}
.main {
}

.element-text30 {
  display: inline-block;
  width: 30%;
  height: 2px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  margin-bottom: 2px;
  margin: 0 4px;
}
.element-text80 {
  width: 80%;
  height: 2px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  margin: 6px;
}
.element-text100 {
  width: 100;
  height: 2px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  margin: 6px;
}
</style>
