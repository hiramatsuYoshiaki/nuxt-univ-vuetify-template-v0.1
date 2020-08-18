<template lang="pug">
  
    v-app
      //- v-navigation-drawer(v-model="drawerLeft" app  mobile-breakpoin="600" left) 
      v-navigation-drawer(v-model="drawerLeft" app   mobile-breakpoin left ) 
        v-card(  height="100%").ps-2.c2  
            h1 xs -600px col10
            h1 sm 600px-960px col0
            h1 md 960px-1264px col0
            h1 lg 1264px-1904px col2
            h1 xl 1904- col2 
      //- v-navigation-drawer(v-model="drawerRight" app  mobile-breakpoin="600" right )
      v-navigation-drawer(v-model="drawerRight" app  mobile-breakpoin right )
        v-card(  height="100%").ps-2.c3  
            h1 xs -600px col10
            h1 sm 600px-960px col0
            h1 md 960px-1264px col0
            h1 lg 1264px-1904px col2
            h1 xl 1904- col2   
      v-main.ma-0.pa-0
        v-container
          //- v-row
          //-       v-col(cols="12" sm="12" md="12" lg="12")
          v-card(height="100%").c1.pa-2 
              h1 Off Canvas (Grid System by Flexbox)
              h3 Components/Grid
              h3 v-container
              nuxt-link(to="/template") 
                h3 back to Nuxt Page Template
              h1 xs -600px col12
              h1 sm 600px-960px col12
              h1 md 960px-1264px col12
              h1 lg 1264px-1904px col8
              h1 xl 1904- col8 
</template>
<script>
export default {
  layout: 'dropdownHeader',
}
</script>
<style lang="scss" scoped>
.c1 {
  background-color: rgba(4, 33, 161, 0.5);
}
.c2 {
  background-color: rgba(3, 151, 250, 0.5);
}
.c3 {
  background-color: rgba(2, 109, 20, 0.5);
}
</style>
