<template lang="pug">
    div.stikyFooter 
        div.header 
            div.element-text30 
        div.main 
            div.element-text100
            div.element-text80
            div.element-text80
        div.footer 
            div.element-text30 
            div.element-text30 
        //- メインコンテンツが短い場合、フッターは常に下部に固定されます。
</template>

<style lang="scss" scoped>
.stikyFooter {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 100%;
}
.header {
  flex-shrink: 0;
  overflow: auto;
  border-bottom: 1px solid rgba(0, 0, 0, 0.3);
}
.main {
  flex-grow: 1;
  overflow: auto;
}
.footer {
  flex-shrink: 0;
  border-top: 1px solid rgba(0, 0, 0, 0.3);
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
