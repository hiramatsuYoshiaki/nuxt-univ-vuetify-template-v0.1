<template lang="pug">
        v-container
            v-row
                v-col
                    h1 UIコンポーネント
            v-row
                v-col
                    nuxt-link(to="/layoutSetting") 
                        h1 Nuxt Layout Setting 
            v-row
                v-col
                    nuxt-link(to="/respPattern") 
                        h1 Responsive Pattern Layout
            v-row
                v-col
                    h1 Bars/App Bars (side bar) 
            v-row
                v-col
                    h1 Bars/ToolBars (header bar) 
            v-row
                v-col
                    h1 カテゴリー
            v-row
                v-col(cols="12" sm="6" v-for="n in 4" :key="n")
                    v-card.pa-2(outlined tile) One of three columns
            v-row
                v-col
                    h1 カテゴリー
            
            

</template>
<script>
export default {
  layout: 'sidebarNav-vuetify',
}
</script>
<style lang="scss" scoped>
// * {
//   border: 1px solid;
// }
</style>
