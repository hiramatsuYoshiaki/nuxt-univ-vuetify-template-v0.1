<template lang="pug">
    v-app(id="baseline")
        v-navigation-drawer(v-model="drawer" app dark mobile-break-point bottom)  
            v-list(dense) 
                v-list-item(link to="/" nuxt) 
                        v-list-item-action 
                                v-icon  fas fa-home 
                        v-list-item-content 
                                v-list-item-title HOME
                v-list-item(link to="/setting" nuxt) 
                        v-list-item-action 
                                v-icon  fas fa-cogs
                        v-list-item-content 
                                v-list-item-title CUSTAM
                v-list-item(link to="/component" nuxt) 
                        v-list-item-action 
                                v-icon  fas fa-cubes
                        v-list-item-content 
                                v-list-item-title COMPONENTS
        v-app-bar(app) 
            v-app-bar-nav-icon(@click.stop="drawer = !drawer") 
            v-toolbar-title Vuetify.js  aaaaaa
            v-spacer 
        v-main
            nuxt 
        v-footer(app)
            v-toolbar-title 
                span CSS Falmework Vuetify.js  
                span &copy; {{ new Date().getFullYear() }} 
        //- v-bottom-navigation(app) bottom-navigation
</template>
<script>
export default {
  data() {
    return {
      drawer: null,
    }
  },
}
</script>
<style lang="scss">
html {
  font-size: 62.5%; //62.5% 1rem=10px
}
</style>
