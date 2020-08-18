<template lang="pug">
    v-container
        v-row
            v-col
                h1 Sticky Sections Layout
                h3 Components / Grids
                v-chip-group(column)  
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col  
                     
        v-row
            v-col(cols="12")
                div.main-wrape.bd-a
                    section.sticky-section.text-h1.grey.lighten-1 section1
                    section.sticky-section.text-h1.grey.lighten-2 section2
                    section.sticky-section.text-h1.grey.lighten-3 section3
                    section.sticky-section.text-h1.grey.lighten-4 section4
                    section.sticky-section.text-h1.grey.lighten-5 section5
                    
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
.main-wrape {
  height: 500px;
  overflow-y: scroll;
}
.sticky-section {
  position: sticky;
  top: 0;
  height: 300px;
}
.bd-a {
  border: 1px solid;
}
</style>
