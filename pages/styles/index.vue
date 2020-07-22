<template lang="pug">
    v-container
        v-row
            v-col
                div.text-h1 STYLES
                div-text-h3 Styles/
                //- div-text-h3 v-navigation-drawer
        v-row
            v-col
                nuxt-link(to="/"  nuxt) 
                    h3 Back to  Nuxt HOME 
</template>
<script>
export default {
  layout: 'sidebarNav-vuetify',
}
</script>
<style lang="scss" scoped>
* {
  border: 1px solid;
}
</style>
