<template lang="pug">
    v-app(id="dropdownHeader")
        v-app-bar(app height="60px")
            v-app-bar-nav-icon(@click.stop="drawer = !drawer").d-block.d-md-none 
            v-toolbar-title
                v-btn(text to="/" nuxt) 
                    img.VuetifyLogo(alt="Vuetify Logo" src="/vuetify-logo.svg" )
                span Drop Down Header 
            v-spacer 
            span( v-for="(item, index) in items" :key="index" @click="" ).d-none.d-md-block
                v-btn(text :to="item.to" nuxt) {{ item.title }}
        div.abu
            v-scroll-y-transition
                //- v-scroll-x-transition
                //- v-scale-transition
                //- v-expand-transition
                //- v-fab-transition
                div( v-show="drawer")
                        v-list.d-block.d-md-none.grey.lighten-1
                            v-list-item( v-for="(item, index) in items" :key="index" @click="" )
                                v-list-item-title 
                                    v-btn(text :to="item.to" nuxt) {{ item.title }}
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
.VuetifyLogo {
  height: 40px;
  width: 40px;
  transform: rotateY(560deg);
  animation: turn 3.5s ease-out forwards 1s;
}

@keyframes turn {
  100% {
    transform: rotateY(0deg);
  }
}
.abu {
  position: absolute;
  top: 0;
  left: 0;
  margin-top: 60px;
  z-index: 1;
  width: 100%;
}
</style>
