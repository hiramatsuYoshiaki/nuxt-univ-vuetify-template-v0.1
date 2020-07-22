<template lang="pug">
        v-container
            v-row
                v-col
                    h1 Side Bar Left
                    h3 Components/Application
                    h3 v-navigation-drawer
            v-row
                v-col
                    nuxt-link(to="/layoutSetting") 
                        h3 back to Nuxt Layout Setting 
</template>
<script>
export default {
  layout: 'fullscreenNav',
}
</script>
<style lang="scss" scoped>
// * {
//   border: 1px solid;
// }
</style>
