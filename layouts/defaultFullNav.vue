<template lang="pug">
    v-app(id="baseline")
        v-system-bar(app  ) 
                v-spacer
                <v-icon>mdi-wifi-strength-4</v-icon>
                <v-icon>mdi-signal-cellular-outline</v-icon>
                <v-icon>mdi-battery</v-icon>
                <span>12:30</span>
        v-navigation-drawer(v-model="drawer" app dark mobile-breakpoint clipped)  
            v-list(dense) 
                v-list-item(v-for="(item,i) in items" :key="i" :to="item.to")
                        v-list-item-action 
                                v-icon  {{item.icon}} 
                        v-list-item-content 
                                v-list-item-title {{item.title}} 
                //- v-list-item(link to="/" nuxt)  
                //-         v-list-item-action 
                //-                 v-icon  fas fa-home 
                //-         v-list-item-content 
                //-                 v-list-item-title HOME
        v-app-bar(app clipped-left) 
            v-app-bar-nav-icon(@click.stop="drawer = !drawer") 
            v-toolbar-title Vuetify.js  
            v-spacer 
        v-main
            nuxt 
        v-footer(app)
            v-toolbar-title 
                span CSS Falmework Vuetify.js  
                span &copy; {{ new Date().getFullYear() }} 
        v-bottom-navigation(app v-model="bottomNav") 
                <v-btn value="home">
                        <span>Home</span>
                        <v-icon>home</v-icon>
                </v-btn>

                <v-btn value="favorites">
                        <span>Ui component</span>
                        <v-icon>fas fa-cubes</v-icon>
                </v-btn>

                <v-btn value="appLayout" to="/appLayout" nuxt >
                        <span>App Layout</span>
                        <v-icon>fas fa-th-large</v-icon>
                </v-btn>
               
</template>
<script>
export default {
  data() {
    return {
      drawer: null,
      bottomNav: 'appLayout',
      items: [
        {
          icon: 'home',
          title: 'HOME',
          to: '/',
        },
        {
          icon: 'fas fa-cubes',
          title: 'UI COMPONENT',
          to: '/component',
        },
        {
          icon: 'fas fa-th-large',
          title: 'APP LAYOUT',
          to: '/appLayout',
        },
        {
          icon: 'far fa-window-maximize',
          title: 'PAGE TENPLATE',
          to: '/template',
        },
      ],
    }
  },
}
</script>
<style lang="scss">
html {
  font-size: 62.5%; //62.5% 1rem=10px
  //   background: $test;
}
// a {
//   color: black;
//   text-decoration: none;
//   cursor: pointer;
//   &:hover {
//     opacity: 0.5;
//   }
// }
</style>
