<template lang="pug">
        v-container
            v-row
                v-col
                    h1 App Layout / defaultFullNav
                    h3 Components / Application
                    h3 v-app-bar
                    h3 v-bottom-navigation
                    h3 v-footer
                    h3 v-navigation-drawer
                    h3 v-system-bar
            v-row
                v-col
                    nuxt-link(to="/appLayout"  nuxt) 
                        h3 Back to  App Layout 
</template>
<script>
export default {
  layout: 'defaultFullNav',
}
</script>
<style lang="scss" scoped>
// * {
//   border: 1px solid;
// }
</style>
