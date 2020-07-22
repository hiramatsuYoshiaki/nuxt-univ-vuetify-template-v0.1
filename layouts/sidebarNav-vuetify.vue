<template lang="pug">
    v-app(id="baseline")
        v-navigation-drawer(v-model="drawer" app dark mobile-breakpoint )  
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
      items: [
        {
          icon: 'home',
          title: 'HOME',
          to: '/',
        },
        {
          icon: 'faf fa-clock',
          title: 'START',
          to: '/start',
        },
        {
          icon: 'fas fa-cog',
          title: 'CUSTOMS',
          to: '/customization',
        },
        {
          icon: 'fas fa-palette',
          title: 'STYLE',
          to: '/styles',
        },
        {
          icon: 'fas fa-cubes',
          title: 'UI COMPONENT',
          to: '/component',
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
