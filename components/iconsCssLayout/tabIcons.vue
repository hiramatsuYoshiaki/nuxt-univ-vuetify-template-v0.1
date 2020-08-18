<template lang="pug">
    div.tab
      div.item-active.item1
        nuxt-link(to="'/cssLayout'")
            div.circle
      div.item.item2
        nuxt-link(to="'/cssLayout'")
            div.circle
      div.item.item3
        nuxt-link(to="'/cssLayout'")
            div.circle
</template>

<style lang="scss" scoped>
.tab {
  /* Content is centered vertically */
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
  padding: 8px;
}
.item-active {
  border-bottom: 1px solid rgba(0, 0, 0, 0);
  border-top: 1px solid rgba(0, 0, 0, 0.3);
  border-left: 1px solid rgba(0, 0, 0, 0.3);
  border-right: 1px solid rgba(0, 0, 0, 0.3);
  border-top-left-radius: 4px;
  border-top-right-radius: 4px;
  //   &:hover {
  //     border-bottom: 1px solid rgba(0, 0, 0, 0.3);
  //     border-top: 1px solid rgba(0, 0, 0, 0);
  //     border-left: 1px solid rgba(0, 0, 0, 0);
  //     border-right: 1px solid rgba(0, 0, 0, 0);
  //     border-top-left-radius: 0px;
  //     border-top-right-radius: 0px;
  //   }
}
.item {
  border-bottom: 1px solid rgba(0, 0, 0, 0.3);
  //   &:hover {
  //     border-bottom: 1px solid rgba(0, 0, 0, 0);
  //     border-top: 1px solid rgba(0, 0, 0, 0.3);
  //     border-left: 1px solid rgba(0, 0, 0, 0.3);
  //     border-right: 1px solid rgba(0, 0, 0, 0.3);
  //     border-top-left-radius: 4px;
  //     border-top-right-radius: 4px;
  //   }
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
.item a,
.item-active a {
  &:hover {
    opacity: 0.5;
    .circle {
      background-color: rgba(0, 0, 0, 0.1);
    }
  }
}
</style>
