<template lang="pug">
    v-container
        v-row
            v-col
                h1 Drop Down Center Menu
                h3 Components/Application
                h3 v-scroll-y-transition
                h3 v-list
        v-row
            v-col
                nuxt-link(to="/appLayout"  nuxt) 
                    h3 Back to  App Layout
</template>
<script>
export default {
  layout: 'dropdownCenterNav',
}
</script>
<style lang="scss" scoped>
// * {
//   border: 1px solid;
// }
</style>
