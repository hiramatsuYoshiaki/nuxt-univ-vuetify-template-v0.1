<template lang="pug">
    v-app(id="baseline")
        v-navigation-drawer(v-model="drawer" app dark mobile-breakpoin bottom stateless width="100%")  
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
                                v-list-item-title SETTING
                v-list-item(link to="/component" nuxt) 
                        v-list-item-action 
                                v-icon  fas fa-cubes
                        v-list-item-content 
                                v-list-item-title COMPONENTS
                v-list-item(link to="/respPattern" nuxt) 
                        v-list-item-action 
                                v-icon  fas fa-stream
                        v-list-item-content 
                                v-list-item-title Responsive
                //- v-list-item(@click.stop="drawer = !drawer")
                //-         v-list-item-action 
                //-                         v-icon far fa-times-circle
                div.closeBtn(@click.stop="drawer = !drawer") 
                        v-icon fas fa-times

        v-app-bar(app) 
            v-app-bar-nav-icon(@click.stop="drawer = !drawer") 
            v-toolbar-title Vuetify.js  
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
// a {
//   color: black;
//   text-decoration: none;
//   cursor: pointer;
//   &:hover {
//     opacity: 0.5;
//   }
// }
.closeBtn {
  position: absolute;
  top: 0;
  right: 0;
  margin: 2rem;
}
</style>
