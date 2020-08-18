<template lang="pug">
    v-container
        v-row
            v-col
                h1 Holy Grail Layout
                h3 Components / Grids
                v-chip-group(column)  
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col  
                //- h3 Components / images
                //-     v-chip-group 
                //-         v-chip(href="https://vuetifyjs.com/ja/components/images/") v-img 
                     
        v-row.bd
            v-col
                //- v-sheet(dark).text-h1.pa-2 Holy Grail Layout header          
                div.text-h1.pa-2 Holy Grail Layout header          
        v-row.bd-x
            v-col(cols="12" md="3")
                div.text-h3 Aside
                div.text-h6 Aside
            v-col(cols="12" md="6").bd-x 
                div.text-h3 Main
                div.text-h6 Main
                div.text-h6 Main
                div.text-h6 Main
                div.text-h6 Main
                div.text-h6 Main
                div.text-h6 Main
                div.text-h6 Main
                div.text-h6 Main
                div.text-h6 Main
                div.text-h6 Main
                div.text-h6 Main
                div.text-h6 Main
                div.text-h6 Main
                div.text-h6 Main
                div.text-h6 Main
            v-col(cols="12" md="3") 
                div.text-h3 Bside
                div.text-h6 Bside
                div.text-h6 Bside
                div.text-h6 Bside
                         
        v-row.bd
            v-col
                div.text-h3.pa-2 footer          
                //-  v-sheet(dark).text-h1.pa-2 Holy Grail Layout footer          
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
.bd {
  border: 1px solid;
}
.bd-x {
  border-right: 1px solid;
  border-left: 1px solid;
}
</style>
