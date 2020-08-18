<template lang="pug">
  div.wrape 
    div.simpleGrid 
      div.cell-30 
      div.cell-remaining 
    div.simpleGrid 
      div.cell-30 
      div.cell-30 
      div.cell-remaining 
    div.simpleGrid 
      div.cell-20 
      div.cell-20 
      div.cell-remaining 
</template>

<style lang="scss" scoped>
.wrape {
  width: 100%;
  height: 100%;
  padding: 20px;
}
.simpleGrid {
  display: flex;
  // margin-left: -8px;
  // margin-right: -8px;
}

.cell-20 {
  flex: 0 0 20%;
  margin-right: 2px;
  margin-left: 2px;
  height: 16px;
  background-color: rgba(0, 0, 0, 0.3);
  margin-bottom: 4px;
  border-radius: 2px;
}
.cell-30 {
  flex: 0 0 30%;
  margin-right: 2px;
  margin-left: 2px;
  height: 16px;
  background-color: rgba(0, 0, 0, 0.3);
  margin-bottom: 4px;
  border-radius: 2px;
}
.cell-remaining {
  flex: 1;
  margin-right: 2px;
  margin-left: 2px;
  height: 16px;
  background-color: rgba(0, 0, 0, 0.3);
  margin-bottom: 4px;
  border-radius: 2px;
}
</style>
