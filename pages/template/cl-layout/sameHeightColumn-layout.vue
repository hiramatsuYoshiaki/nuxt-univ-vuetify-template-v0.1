<template lang="pug">
    v-container
        v-row
            v-col
                h1 Same Height Column
                h3 Components / Grids
                v-chip-group(column)  
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col  
                h3 Components / Cards
                    v-chip-group(column)  
                        v-chip(href="https://vuetifyjs.com/ja/components/cards/") v-card 
                        v-chip(href="https://vuetifyjs.com/ja/components/cards/") v-card-title 
                        v-chip(href="https://vuetifyjs.com/ja/components/cards/") v-card-subtitle 
                        v-chip(href="https://vuetifyjs.com/ja/components/cards/") v-card-text 
                        v-chip(href="https://vuetifyjs.com/ja/components/cards/") v-card-action
                h3 Components / images
                    v-chip-group 
                        v-chip(href="https://vuetifyjs.com/ja/components/images/") v-img 
                     
                   
        v-row
            v-col
                div.d-flex.flex-wrape
                    v-card(width="300" v-for="i in 4" :key="i" cols="12").mx-2
                        v-img( :src="`https://picsum.photos/200/300?random=${i}`"
                            :lazy-src="`https://picsum.photos/200/300?random=${i}`"
                            aspect-ratio="1"
                            alt="randam images"
                        )
                        v-card-title.text-h1 title {{i}}
                        v-card-subtitle.text-h3 subtitle {{i}}
                        div.ml-4.mb-4 
                            c-card-text.text-h5 text line {{i}}
                            c-card-text.text-h5(v-if="i > 0") text line no.{{i}}
                            c-card-text.text-h5(v-if="i> 1") text line text line text line text line text line text line
                            c-card-text.text-h5(v-if="i> 2") text line text line text line text line text line text line text line text line text line text line text line text line text line
                            c-card-text.text-h5(v-if="i> 3") text line text line text line text line text line text line text line text line text line text line text line text line text line
                            c-card-text.text-h5(v-if="i> 4") text line text line text line text line text line text line text line text line text line text line text line text line text line
                        div.ml-4.mb-4
                            c-card-action
                                v-btn(text).orange.mr-2 share 
                                v-btn(text).orange explore
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
</style>
