<template lang="pug">
    v-container
        v-row
            v-col
                div
                v-breadcrumbs( :items="items" large)
        v-row
            v-col
                div.text-h1 START GUID
                div-text-h3 Getting Started/Quick Start
                //- div-text-h3 v-navigation-drawer
        v-row
            v-col
                nuxt-link(to="/"  nuxt) 
                    h3 Back to  Nuxt HOME 
</template>
<script>
export default {
  layout: 'sidebarNav-vuetify',
  data() {
    return {
      items: [
        {
          text: 'Getting Started',
          disabled: false,
          href: 'breadcrumbs_dashboard',
        },
        {
          text: 'Quick Start',
          disabled: false,
          href: 'breadcrumbs_link_1',
        },
      ],
    }
  },
}
</script>
<style lang="scss" scoped>
* {
  border: 1px solid;
}
</style>
