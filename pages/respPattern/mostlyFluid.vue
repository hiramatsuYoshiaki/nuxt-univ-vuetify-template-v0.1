<template lang="pug">
    v-container.columns
        v-row
              v-col(cols="12" sm="12" md="12" lg="7")
                  v-card.ps-2(outline tile height="25rem").c1  
                      h1 Mostly Fluid (Grid System by Flexbox)
                      h3 Components/Grid
                      h3 v-container
                      nuxt-link(to="/template") 
                        h3 back to Nuxt Page Template
                      h1 xs -600px col12
                      h1 sm 600px-960px col12
                      h1 md 960px-1264px col12
                      h1 lg 1264px-1904px col7
                      h1 xl 1904- col7
              v-col(cols="12" sm="6" md="6" lg="5")
                  v-card.ps-2(outline tile height="25rem").c2  
                      h1 xs -600px col12
                      h1 sm 600px-960px col6
                      h1 md 960px-1264px col6
                      h1 lg 1264px-1904px col3
                      h1 xl 1904- col2
              v-col(cols="12" sm="6" md="6" lg="4")
                  v-card.ps-2(outline tile height="25rem").c3  
                      h1 xs -600px col12
                      h1 sm 600px-960px col6
                      h1 md 960px-1264px col6
                      h1 lg 1264px-1904px col4
                      h1 xl 1904- col4
              v-col(cols="12" sm="6" md="6" lg="4")
                  v-card.ps-2(outline tile height="25rem").c4  
                      h1 xs -600px col12
                      h1 sm 600px-960px col6
                      h1 md 960px-1264px col6
                      h1 lg 1264px-1904px col4
                      h1 xl 1904- col4
              v-col(cols="12" sm="6" md="6" lg="4")
                  v-card.ps-2(outline tile height="25rem").c5   
                      h1 xs -600px col12
                      h1 sm 600px-960px col6
                      h1 md 960px-1264px col6
                      h1 lg 1264px-1904px col4
                      h1 xl 1904- col4
</template>
<script>
export default {
  layout: 'dropdownHeader',
}
</script>
<style lang="scss" scoped>
.columns {
  border: 1px solid grey;
}
.c1 {
  background-color: rgba(4, 33, 161, 0.5);
}
.c2 {
  background-color: rgba(3, 151, 250, 0.5);
}
.c3 {
  background-color: rgba(2, 109, 20, 0.5);
}
.c4 {
  background-color: rgba(163, 134, 4, 0.5);
}
.c5 {
  background-color: rgba(141, 5, 11, 0.5);
}
</style>
