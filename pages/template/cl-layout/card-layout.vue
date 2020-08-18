<template lang="pug">
    v-container
        v-row
            v-col
                h1 Card Layout
                h3 Components / Grids
                v-chip-group(column)  
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col  
                //- h3 Components / Cards
                //-     v-chip-group 
                //-         v-chip(href="https://vuetifyjs.com/ja/components/cards/") v-card 
                h3 Components / images
                    v-chip-group 
                        v-chip(href="https://vuetifyjs.com/ja/components/images/") v-img 
                     
                   
        v-row
            v-col(v-for="i in 6" :key="i" cols="12" md="4")
                //- v-card.mx-auto(max-width="400" ) 
                v-img( :src="`https://picsum.photos/200/300?random=${i}`"
                    :lazy-src="`https://picsum.photos/200/300?random=${i}`"
                    aspect-ratio="1"
                    alt="randam images"
                )
                    //- v-img( :src="`https://picsum.photos/500/300?image=${i * 5 + 10}`"
                    //-     :lazy-src="`https://picsum.photos/10/6?image=${i  * 5 + 10}`"
                    //-     aspect-ratio="1"
                    //- )
                    //- v-img( :src="`https://picsum.photos/id/${i*5+10}/200/300`"
                    //-     :lazy-src="`https://picsum.photos/id/${i*5+10}/200/300`"
                    //-     aspect-ratio="1"
                    //- )
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
