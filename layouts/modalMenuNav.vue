<template lang="pug">
    v-app(id="dropdownHeader")
        v-app-bar(app height="60px")
            v-app-bar-nav-icon(@click.stop="overlay = !overlay").d-block.d-md-none 
            v-toolbar-title
                //- v-btn(text to="/" nuxt) Vuetify.js
                v-btn(text to="/" nuxt) 
                    img.VuetifyLogo(alt="Vuetify Logo" src="/vuetify-logo.svg" )
                span Full Screen Menu  
            v-spacer 
            span( v-for="(item, index) in items" :key="index" @click="" ).d-none.d-md-block
                v-btn(text :to="item.to" nuxt) {{ item.title }}
        v-main
            nuxt 
        v-footer(app)
            v-toolbar-title 
              div.footer-element
                span CSS Falmework Vuetify.js  
                span &copy; {{ new Date().getFullYear() }} 
        v-overlay( :value="overlay" opacity="0.7")
            div.mobile-menu.d-flex.justify-content.align-center.flex-column
              div(v-for="(item, index) in items" :key="index" @click="")
                v-btn(text :to="item.to" nuxt) {{ item.title }}
              v-btn(text)
                icon( @click="overlay = false")
                  v-icon fas fa-times
</template>
<script>
export default {
  data() {
    return {
      overlay: null,
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

.footer-element {
  width: 100%;
  height: 26px;
}
.overlay-wrape {
  border: 1px solid red;
  width: 100vw;
  height: 100vh;
}
.close-btn {
  position: absolute;
  top: 0;
  right: 0;
}
</style>
