<template lang="pug">
    div.stickySections
        
        section.sec1
            div.element-text30
            div.element-text30
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
        section.sec2
            div.element-text30
            div.element-text30
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
        section.sec3
            div.element-text30
            div.element-text30
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            div.element-text80
            
        //- メインコンテンツをスクロールして、各セクションがページの上部にくっついていることを確認してください。
</template>

<style lang="scss" scoped>
.stickySections {
  width: 100%;
  height: 100%;
  overflow: scroll;
}
section {
  /* Take full size */
  height: 100%;
  width: 100%;

  /* Stick to the top */
  position: sticky;
  top: 0;
  padding-top: 2px;
}
.sec1 {
  background-color: white;
}
.sec2 {
  background-color: rgba(0, 0, 0, 0.3);
}
.sec3 {
  background-color: rgba(0, 0, 0, 0.5);
}

.element-text30 {
  width: 30%;
  height: 2px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  margin: 6px;
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
