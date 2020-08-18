<template lang="pug">
    div.pagenation
      div.item-left 
        div.circle
      div.item 
        div.circle
      div.item-right 
        div.circle
</template>

<style lang="scss" scoped>
.pagenation {
  /* Content is centered vertically */
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
  padding: 8px;
}
.item {
  border: 1px solid rgba(0, 0, 0, 0.3);
}
.item-left {
  border-left: 1px solid rgba(0, 0, 0, 0.3);
  border-top: 1px solid rgba(0, 0, 0, 0.3);
  border-bottom: 1px solid rgba(0, 0, 0, 0.3);
  border-top-left-radius: 9999px;
  border-bottom-left-radius: 9999px;
}
.item-right {
  border-right: 1px solid rgba(0, 0, 0, 0.3);
  border-top: 1px solid rgba(0, 0, 0, 0.3);
  border-bottom: 1px solid rgba(0, 0, 0, 0.3);
  border-top-right-radius: 9999px;
  border-bottom-right-radius: 9999px;
}
.circle {
  /* Rounded border */
  border-radius: 9999px;
  height: 10px;
  width: 10px;
  /* OPTIONAL: Spacing between circle */
  margin: 6px;
  background-color: rgba(0, 0, 0, 0.3);
}
</style>
