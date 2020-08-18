<template lang="pug">
    div.PreviousAndNextButtons
      nuxt-link(to="/cssLayout").arrow &lt; prev
      nuxt-link(to="/cssLayout").arrow next &gt;
</template>

<style lang="scss" scoped>
.PreviousAndNextButtons {
  /* Content is centered vertically */
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  height: 100%;
  padding: 8px;
}
.arrow {
  width: 36px;
  height: 36px;
  background-color: white;
  color: black;
  border: 1px solid rgba(0, 0, 0, 0.3);
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 8px;
}
a {
  &:hover {
    opacity: 0.6;
  }
}
</style>
