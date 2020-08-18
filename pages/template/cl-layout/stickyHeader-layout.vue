<template lang="pug">
    v-container
        v-row
            v-col
                h1 Sticky Header Layout
                h3 Components / Grids
                v-chip-group(column) 
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col  
                //- h3 Components / images
                //-     v-chip-group 
                //-         v-chip(href="https://vuetifyjs.com/ja/components/images/") v-img 
                     
        v-row
            v-col(cols="12")
                div.main-wrape.bd-a
                    div.sticky-header.text-h1 header
                    div
                        div.text-h1 main
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                        div.text-h6 Sticky Header Layout
                    
        v-row
            v-col
                nuxt-link(to="/template"  nuxt) 
                    h3 Back to  Page Template
</template>
<script>
export default {
  layout: 'dropdownHeader',
}
</script>
<style lang="scss" scoped>
// * {
//   border: 1px solid;
// }
.main-wrape {
  height: 500px;
  overflow-y: scroll;
}
.sticky-header {
  position: sticky;
  top: 0;
  background-color: lightgrey;
}
.bd-a {
  border: 1px solid;
}
</style>
