<template lang="pug">
    v-container
        v-row
            v-col
                h1 Sticky Footer Layout
                h3 Components / Grids
                v-chip-group(column)  
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col  
        v-row
            v-col(cols="12").d-flex.flex-column.main-content
               div.text-h1.flex-shrink-0.bd-a.pa-2 header
               div.text-h1.flex-grow-1.bd-x.pa-2 main
               div.text-h1.flex-shrink-0.bd-a.pa-2 Sticky Footer
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
.main-content {
  height: 500px;
}
.bd-a {
  border: 1px solid;
}
.bd-x {
  border-right: 1px solid;
  border-left: 1px solid;
}
</style>
