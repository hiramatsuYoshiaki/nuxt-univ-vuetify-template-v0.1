<template lang="pug">
    v-container
        v-row
            v-col
                h1 Simple Grid Layout
                h3 Components / Grids
                v-chip-group(column)  
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col  
                //- h3 Components / images
                //-     v-chip-group 
                //-         v-chip(href="https://vuetifyjs.com/ja/components/images/") v-img 
                     
        v-row.px-25par
            v-col(cols="12" md="4")
                v-sheet(dark height="100" rounded).text-h3.text-md-h6.pa-2 Simple Grid
            v-col(cols="12" md="8")
                v-sheet(dark height="100" rounded).text-h3.text-md-h6.pa-2 Simple Grid
        v-row.px-25par
            v-col(cols="12" md="4")
                 v-sheet(dark height="100" rounded).text-h3.text-md-h6.pa-2 Simple Grid
            v-col(cols="12" md="4")
                 v-sheet(dark height="100" rounded).text-h3.text-md-h6.pa-2 Simple Grid
            v-col(cols="12" md="4")
                 v-sheet(dark height="100" rounded).text-h3.text-md-h6.pa-2 Simple Grid
        
        v-row.px-25par
            v-col(cols="12" md="3")
                 v-sheet(dark height="100" rounded).text-h3.text-md-h6.pa-2 Simple Grid
            v-col(cols="12" md="3")
                 v-sheet(dark height="100" rounded).text-h3.text-md-h6.pa-2 Simple Grid
            v-col(cols="12" md="6")
                 v-sheet(dark height="100" rounded).text-h3.text-md-h6.pa-2 Simple Grid
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
.px-25par {
  padding: 0 25%;
}
</style>
