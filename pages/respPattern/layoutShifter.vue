<template lang="pug">
        v-container(class="grey lighten-5")
            v-row
                v-col(cols="12" sm="12" md="12" lg="3" xl="3")
                    v-card.ps-2(outline tile ).menu 
                        h1 Layout Shifter (Grid System by Flexbox)
                        h3 Components/Grid
                        h3 v-container
                        nuxt-link(to="/respPattern") 
                            h3 back to Nuxt Responsive Pattern
                        h1 xs -600px col12
                        h1 sm 600px-960px col12
                        h1 md 960px-1264px col12
                        h1 lg 1264px-1904px col3
                        h1 xl 1904- col3
                v-col(cols="12" sm="12" md="12" lg="9" xl="9")
                    v-row(no-gutters) 
                        v-col(cols="12")
                            v-card.ps-2.mb-2(outline tile height="25rem") 
                                h1 xs -600px col12
                                h1 sm 600px-960px col12
                                h1 md 960px-1264px col12
                                h1 lg 1264px-1904px col9
                                h1 xl 1904- col9
                        v-col(cols="12")
                            v-card.ps-2.mb-2(outline tile height="25rem") 
                                h1 xs -600px col12
                                h1 sm 600px-960px col12
                                h1 md 960px-1264px col12
                                h1 lg 1264px-1904px col9
                                h1 xl 1904- col9 
                
               
</template>
<script>
export default {
  layout: 'fullscreenNav',
}
</script>
<style lang="scss" scoped>
.menu {
  height: 25rem;
  @media (min-width: 1264px) {
    height: 100vh;
  }
}
</style>
