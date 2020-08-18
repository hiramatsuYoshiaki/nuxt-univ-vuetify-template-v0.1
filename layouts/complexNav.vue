<template lang="pug">
    v-app(id="baseline")
        v-navigation-drawer(v-model="drawerLeft" app dark mobile-breakpoin left)  
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
        v-navigation-drawer(v-model="drawerRight" app dark mobile-breakpoin right clipped)  
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
        v-app-bar(app clipped-right) 
            v-app-bar-nav-icon(@click.stop="drawerLeft = !drawerLeft") 
            v-toolbar-title Vuetify.js  complex
            v-spacer 
            v-app-bar-nav-icon(@click.stop="drawerRight = !drawerRight") 
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
      drawerLeft: null,
      drawerRight: null,
    }
  },
}
</script>
<style lang="scss">
html {
  font-size: 62.5%; //62.5% 1rem=10px
}
</style>
