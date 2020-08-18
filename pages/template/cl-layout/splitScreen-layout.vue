<template lang="pug">
    v-container
        v-row
            v-col
                h1 Sprit Screen Layout
                h3 Components / Grids
                v-chip-group(column)  
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col  
                h3 Components / images
                    v-chip-group(column)  
                        v-chip(href="https://vuetifyjs.com/ja/components/images/") v-img 
                     
        v-row.bd
            //- v-col(cols="12" sm="6").d-flex.justyfy-center.align-center
            v-col(cols="6" sm="6").d-flex.align-center.justify-center.bd-r
                v-img( :src="`https://picsum.photos/200/200?random=1`"
                            :lazy-src="`https://picsum.photos/200/200?random=1`"
                            aspect-ratio="1"
                            alt="randam images"
                            max-width="200"
                            max-height="200"
                        )
            v-col(cols="6" sm="6")
                div.text-h3 Sprit Screen Layout
                div.text-h6 Side-A 50% / side-B 50% 
                div.text-h6 Side-A 50% / side-B 50% 
                div.text-h6 Side-A 50% / side-B 50% 
                div.text-h6 Side-A 50% / side-B 50% 
                div.text-h6 Side-A 50% / side-B 50% 
                div.text-h6 Side-A 50% / side-B 50% 
                div.text-h6 Side-A 50% / side-B 50% 
                div.text-h6 Side-A 50% / side-B 50% 
                div.text-h6 Side-A 50% / side-B 50% 
                div.text-h6 Side-A 50% / side-B 50% 
                div.text-h6 Side-A 50% / side-B 50% 
                div.text-h6 Side-A 50% / side-B 50% 
                div.text-h6 Side-A 50% / side-B 50% 
                div.text-h6 Side-A 50% / side-B 50% 
                div.text-h6 Side-A 50% / side-B 50% 
                div.text-h6 Side-A 50% / side-B 50% 
                div.text-h6 Side-A 50% / side-B 50% 
                div.text-h6 Side-A 50% / side-B 50% 
                div.text-h6 Side-A 50% / side-B 50% 
                div.text-h6 Side-A 50% / side-B 50% 
                div.text-h6 Side-A 50% / side-B 50% 
                div.text-h6 Side-A 50% / side-B 50% 
                 
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
.bd-r {
  border-right: 1px solid;
}
</style>
