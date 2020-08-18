<template lang="pug">
    div.dotNavigation 
        div.circle.circle-inactive
        div.circle.circle-active
        div.circle.circle-inactive
        div.circle.circle-inactive
        
</template>

<style lang="scss" scoped>
// * {
//   border: 1px dotted grey;
// }
.dotNavigation {
  /* Content is centered vertically */
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
  padding: 8px;
}
.circle {
  /* Rounded border */
  border-radius: 9999px;
  height: 10px;
  width: 10px;
  /* OPTIONAL: Spacing between dots */
  margin: 0 4px;
}
.circle-active {
  /* Active dot */
  background-color: rgba(0, 0, 0, 0.3);
}
.circle-inactive {
  /* Inactive dot */
  background-color: transparent;
  border: 1px solid rgba(0, 0, 0, 0.3);
}
</style>
