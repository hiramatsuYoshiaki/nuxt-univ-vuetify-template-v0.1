<template lang="pug">
        v-container
            v-row
                v-col
                    h1 Side Bar Bottom (mobile)
                    h3 Components/Application
                    h3 v-navigation-drawer
            v-row
                v-col
                    nuxt-link(to="/layoutSetting") 
                        h3 Back to  Nuxt Layout Setting 
</template>
<script>
export default {
  layout: 'sidebarBottomNav',
}
</script>
<style lang="scss" scoped>
// * {
//   border: 1px solid;
// }
</style>
