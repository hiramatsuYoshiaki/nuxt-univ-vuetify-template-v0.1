<template lang="pug">
    v-container
        v-row
            v-col
                h1 Modal menu
                h3 Components/Application
                h3 v-overlay
        v-row
            v-col
                nuxt-link(to="/appLayout"  nuxt) 
                    h3 Back to  App Layout
</template>
<script>
export default {
  layout: 'modalMenuNav',
}
</script>
<style lang="scss" scoped>
// * {
//   border: 1px solid;
// }
</style>
