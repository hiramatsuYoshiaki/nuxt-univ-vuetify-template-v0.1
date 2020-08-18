<template lang="pug">
v-container(fluid)
    v-row 
        v-col(cols="12")
            div.text-h1.mb-4 App Layout
            div.text-h3.pa-4 サイドバー
    v-row
        v-col(cols="12" sm="12" md="6" lg="6" xl="4")
                v-card(color="grey lighten-3").pa-6 
                    div(class="d-flex flex-no-wrap justify-space-between")
                        div.flex-grow-0.flex-shrink-0   
                            v-card-title.headline 
                                 nuxt-link(to="template/defaultFull") Full Component 
                            v-card-subtitle Application コンポーネントすべてを使用 
                            v-card-subtitle
                                nuxt-link(to="template/defaultFull")
                                    div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0         
                                        div.card-element
                                                component( :is="'defaultFull'" )
                            v-card-actions
                            v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                        div.flex-grow-1.flex-shrink-1   
                            v-card-title.headline.font-weight-bold Component
                            v-card-subtitle 
                                a(href="https://vuetifyjs.com/ja/components/app-bars/" target="_blank")
                                    div.text-h5 v-app-bar
                                a(href="https://vuetifyjs.com/ja/components/bottom-navigation/" target="_blank")
                                    div.text-h5 v-bottom-navigation
                                a(href="https://vuetifyjs.com/ja/components/footer/" target="_blank")
                                    div.text-h5 v-footer
                                a(href="https://vuetifyjs.com/ja/components/navigation-drawers/" target="_blank")
                                    div.text-h5 v-navigation-drawer
                                a(href="https://vuetifyjs.com/ja/components/system-bars/" target="_blank")
                                    div.text-h5 v-system-bar
        v-col(cols="12" sm="12" md="6" lg="6" xl="4")
                v-card(color="grey lighten-3").pa-6 
                    div(class="d-flex flex-no-wrap justify-space-between")
                        div.flex-grow-0.flex-shrink-0   
                            v-card-title.headline 
                                 nuxt-link(to="template/baseline") Baseline 
                            v-card-subtitle Application コンポーネント
                            v-card-subtitle
                                nuxt-link(to="template/baseline")
                                    div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0         
                                        div.card-element
                                                component( :is="'baseline'" )
                            v-card-actions
                            v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                        div.flex-grow-1.flex-shrink-1   
                            v-card-title.headline.font-weight-bold Component
                            v-card-subtitle 
                                a(href="https://vuetifyjs.com/ja/components/app-bars/" target="_blank")
                                    div.text-h5 v-app-bar
                                a(href="https://vuetifyjs.com/ja/components/footer/" target="_blank")
                                    div.text-h5 v-footer
                                a(href="https://vuetifyjs.com/ja/components/navigation-drawers/" target="_blank")
                                    div.text-h5 v-navigation-drawer
        v-col(cols="12" sm="12" md="6" lg="6" xl="4")
                v-card(color="grey lighten-3").pa-6 
                    div(class="d-flex flex-no-wrap justify-space-between")
                        div.flex-grow-0.flex-shrink-0   
                            v-card-title.headline 
                                 nuxt-link(to="template/complex") Complex
                            v-card-subtitle Application コンポーネント
                            v-card-subtitle
                                nuxt-link(to="template/complex")
                                    div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0         
                                        div.card-element
                                                component( :is="'complex'" )
                            v-card-actions
                            v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                        div.flex-grow-1.flex-shrink-1   
                            v-card-title.headline.font-weight-bold Component
                            v-card-subtitle 
                                a(href="https://vuetifyjs.com/ja/components/app-bars/" target="_blank")
                                    div.text-h5 v-app-bar
                                a(href="https://vuetifyjs.com/ja/components/footer/" target="_blank")
                                    div.text-h5 v-footer
                                a(href="https://vuetifyjs.com/ja/components/navigation-drawers/" target="_blank")
                                    div.text-h5 v-navigation-drawer
        
    v-row 
        v-col(cols="12")
            div.text-h3.pa-4 ドロップダウン
    v-row
        v-col(cols="12" sm="12" md="6" lg="6" xl="4")
                v-card(color="grey lighten-3").pa-6 
                    div(class="d-flex flex-no-wrap justify-space-between")
                        div.flex-grow-0.flex-shrink-0   
                            v-card-title.headline 
                                 nuxt-link(to="template/dropdownHeader") Dropdown top 
                            v-card-subtitle Application コンポーネント
                            v-card-subtitle
                                nuxt-link(to="template/dropdownHeader")
                                    div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0         
                                        div.card-element
                                                component( :is="'dropdownHeader'" )
                            v-card-actions
                            v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                        div.flex-grow-1.flex-shrink-1   
                            v-card-title.headline.font-weight-bold Component
                            v-card-subtitle 
                                a(href="https://vuetifyjs.com/ja/components/app-bars/" target="_blank")
                                    div.text-h5 v-app-bar
                                a(href="https://vuetifyjs.com/ja/components/footer/" target="_blank")
                                    div.text-h5 v-footer
        v-col(cols="12" sm="12" md="6" lg="6" xl="4")
                    v-card(color="grey lighten-3").pa-6 
                        div(class="d-flex flex-no-wrap justify-space-between")
                            div.flex-grow-0.flex-shrink-0   
                                v-card-title.headline 
                                    nuxt-link(to="template/dropdownCenter") Dropdown Center
                                v-card-subtitle Application コンポーネント
                                v-card-subtitle
                                    nuxt-link(to="template/dropdownCenter")
                                        div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0         
                                            div.card-element
                                                    component( :is="'dropdownCenter'" )
                                v-card-actions
                                v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                            div.flex-grow-1.flex-shrink-1   
                                v-card-title.headline.font-weight-bold Component
                                v-card-subtitle 
                                    a(href="https://vuetifyjs.com/ja/components/app-bars/" target="_blank")
                                        div.text-h5 v-app-bar
                                    a(href="https://vuetifyjs.com/ja/components/footer/" target="_blank")
                                        div.text-h5 v-footer        
    v-row 
        v-col(cols="12")
            div.text-h3.pa-4 モーダル
    v-row 
        v-col(cols="12" sm="12" md="6" lg="6" xl="4")
                    v-card(color="grey lighten-3").pa-6 
                        div(class="d-flex flex-no-wrap justify-space-between")
                            div.flex-grow-0.flex-shrink-0   
                                v-card-title.headline 
                                    nuxt-link(to="template/modalMenu") Modal Menu
                                v-card-subtitle Application コンポーネント
                                v-card-subtitle
                                    nuxt-link(to="template/modalMenu")
                                        div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0         
                                            div.card-element
                                                    component( :is="'modalMenu'" )
                                v-card-actions
                                v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                            div.flex-grow-1.flex-shrink-1   
                                v-card-title.headline.font-weight-bold Component
                                v-card-subtitle 
                                    a(href="https://vuetifyjs.com/ja/components/app-bars/" target="_blank")
                                        div.text-h5 v-app-bar
                                    a(href="https://vuetifyjs.com/ja/components/footer/" target="_blank")
                                        div.text-h5 v-footer                              
</template>
<script>
import defaultFull from '~/components/iconsCssLayout/defaultFull.vue'
import holyGrailIcons from '~/components/iconsCssLayout/holyGrailIcons.vue'
import dropdownHeader from '~/components/iconsCssLayout/dropdownHeader.vue'
import baseline from '~/components/iconsCssLayout/baseline.vue'
import complex from '~/components/iconsCssLayout/complex.vue'
import dropdownCenter from '~/components/iconsCssLayout/dropdownCenter.vue'
import modalMenu from '~/components/iconsCssLayout/modalMenu.vue'

export default {
  layout: 'sidebarNav-vuetify',
  components: {
    defaultFull,
    holyGrailIcons,
    dropdownHeader,
    baseline,
    complex,
    dropdownCenter,
    modalMenu,
  },
  //   data() {
  //     return {
  //       collections: [
  //         {
  //           id: 1002,
  //           category: 'layout',
  //           name: 'Holy grail',
  //           components: 'holyGrail',
  //         },
  //       ],
  //     }
  //   },
}
</script>
<style scoped lang="scss">
.card-element {
  border: 1px solid rgba(0, 0, 0, 0.3);
  border-radius: 2px;
  box-shadow: rgba(0, 0, 0, 0.2) 0px 16px 24px -4px,
    rgba(0, 0, 0, 0.05) 0px 8px 8px -4px;
  height: 160px;
  width: 160px;
  overflow: hidden;
  position: relative;
}
</style>
