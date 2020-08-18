<template lang="pug">
  div.circularNavigation
    div.menu-item
    div.menu-item.item1.menu-item-radius
      div.menu-inner.inner-item-roate1 1
    div.menu-item.item2.menu-item-radius
      div.menu-inner.inner-item-roate2 2
    div.menu-item.item3.menu-item-radius
      div.menu-inner.inner-item-roate3 3
    div.menu-item.item4.menu-item-radius
      div.menu-inner.inner-item-roate4 4
    div.menu-item.item5.menu-item-radius
      div.menu-inner.inner-item-roate5 5
    div.menu-item.item6.menu-item-radius
     div.menu-inner.inner-item-roate6 6
</template>

<style lang="scss" scoped>
.circularNavigation {
  position: relative;
  width: 100%;
  height: 100%;
}
.menu-item {
  position: absolute;
  top: 50%;
  left: 50%;
  // transform: rotate(0deg) translateX(-40px);
  height: 16px;
  width: 16px;
  background-color: rgba(0, 0, 0, 0.3);
  margin-top: -8px;
  margin-left: -8px;
}
.menu-item-radius {
  border-radius: 9999px;
}
.item1 {
  transform: rotate(0deg) translateX(30px);
}
.item2 {
  transform: rotate(60deg) translateX(30px);
}
.item3 {
  transform: rotate(120deg) translateX(30px);
}
.item4 {
  transform: rotate(180deg) translateX(30px);
}
.item5 {
  transform: rotate(240deg) translateX(30px);
}
.item6 {
  transform: rotate(300deg) translateX(30px);
}
// .item6 {
//   transform: rotate(0deg) translateX(30px);
// }
.menu-inner {
  height: 100%;
  width: 100%;
  transform: rotate(-0deg);
  align-items: center;
  display: flex;
  justify-content: center;
  color: white;
}
.inner-item-roate1 {
  transform: rotate(-0deg);
}
.inner-item-roate2 {
  transform: rotate(-60deg);
}
.inner-item-roate3 {
  transform: rotate(-120deg);
}
.inner-item-roate4 {
  transform: rotate(-180deg);
}
.inner-item-roate5 {
  transform: rotate(-240deg);
}
.inner-item-roate6 {
  transform: rotate(-300deg);
}
</style>
