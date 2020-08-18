<template lang="pug">
  div.someHeightColumn
    div.section-column
        div.content-heigher 
        div.main-content
            .element-title60
            .element-text30
            .element-text80
            .element-text60
        //- div.btn--default.btn
    div.section-column
        div.content-heigher 
        div.main-content
            .element-title60
            .element-text30
            .element-text80
            .element-text60
            .element-text60
            .element-text30
            .element-text80
            .element-text60
            .element-text30
            .element-text80
            .element-text80
            .element-text80
       
        //- div.btn--default.btn
</template>

<style lang="scss" scoped>
.someHeightColumn {
  display: flex;
  //   flex-direction: column;
  width: 100%;
  height: 100%;
}
.section-column {
  flex: 1;
  /* Space between columns */
  margin: 4px 4px;

  /* Layout each column */
  display: flex;
  flex-direction: column;
}
.content-heigher {
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 5px;
  height: 40px;
}
.main-content {
  padding: 4px 4px 24px 4px;
  flex: 1;
}
.btn {
  width: 16px;
  height: 4px;
  margin: 2px;
  color: #fff;
}

.element-text30 {
  width: 30%;
  height: 2px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  margin-bottom: 2px;
}
.element-text80 {
  width: 80%;
  height: 2px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  margin-bottom: 2px;
}
.element-text60 {
  width: 60%;
  height: 2px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  margin-bottom: 2px;
}
.element-title60 {
  width: 60%;
  height: 4px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  margin-bottom: 2px;
}
</style>
