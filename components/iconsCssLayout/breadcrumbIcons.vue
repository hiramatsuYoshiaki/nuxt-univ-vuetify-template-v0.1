<template lang="pug">
    div.breadcrumb 
        nuxt-link.link(to="/cssLayout")
            div.element-text
        div.separator /
        nuxt-link(to="/cssLayout")
            div.element-text
        div.separator /
        nuxt-link(to="/cssLayout")
            div.element-text
</template>

<style lang="scss" scoped>
.breadcrumb {
  /* Content is centered vertically */
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
  padding: 8px;
}
.separator {
  margin: 0 4px;
}
.element-text {
  width: 16px;
  height: 12px;
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 2px;
}
a {
  &:hover {
    opacity: 0.6;
  }
}
</style>
