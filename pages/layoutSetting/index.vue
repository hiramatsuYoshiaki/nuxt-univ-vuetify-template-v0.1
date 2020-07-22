<template lang="pug">
        v-container
            v-row
                v-col
                    h1 Nuxt Layout Setting
            v-row
                v-col
                    nuxt-link(to="/layoutSetting/sidebarLeft") 
                        h1  Side NavBar Left (Application/Navigation Drawers) 
            v-row
                v-col
                    nuxt-link(to="/layoutSetting/sidebarBottom") 
                        h1  Side NavBar Bottom (Application/Navigation Drawers) 
            v-row
                v-col
                    nuxt-link(to="/layoutSetting/fullscreen") 
                        h1  Full Screen NavBar (Application/Navigation Drawers)   
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
