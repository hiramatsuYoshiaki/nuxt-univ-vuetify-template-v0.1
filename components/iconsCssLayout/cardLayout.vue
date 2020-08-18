<template lang="pug">
    div.cardLayout 
        div.cardLayout-card
        div.cardLayout-card
        div.cardLayout-card
        div.cardLayout-card
        div.cardLayout-card
        div.cardLayout-card
        div.cardLayout-card
        div.cardLayout-card
        div.cardLayout-card
        //- div {{title}}
       
        
</template>
<style lang="scss" scoped>
.cardLayout {
  display: flex;
  flex-wrap: wrap;
  //   margin-left: -8px;
  //   margin-right: -8px;
  padding: 20px;
  width: 100%;
  height: 100%;
}
.cardLayout-card {
  flex-basis: 25%;
  //   margin-left: 8px;
  //   margin-right: 8px;
  height: 26px;
  margin-bottom: 4px;
  margin-right: 4px;
  margin-left: 4px;
  background-color: rgba(0, 0, 0, 0.3);
}
</style>
