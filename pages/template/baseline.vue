<template lang="pug">
        v-container
            v-row
                v-col
                    h1 App Layout / Baseline
                    h3 Components / Application
                    h3 v-app-bar
                    h3 v-footer
                    h3 v-navigation-drawer
            v-row
                v-col
                    nuxt-link(to="/appLayout"  nuxt) 
                        h3 Back to  App Layout 
</template>
<script>
export default {
  layout: 'baseline',
}
</script>
<style lang="scss" scoped>
// * {
//   border: 1px solid;
// }
</style>
