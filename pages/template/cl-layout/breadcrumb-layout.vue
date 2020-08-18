<template lang="pug">
    v-container
        v-row
            v-col
                h1 breadcrumbs
                v-chip-group(column) 
                    v-chip(href="https://vuetifyjs.com/ja/components/breadcrumbs/") v-breadcrumbs 
                    v-chip(href="https://vuetifyjs.com/ja/components/breadcrumbs/") v-breadcrumbs-item
        v-row
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader.text-h3 Large
                    v-divider
                    div 
                        v-breadcrumbs( :items="items")
                    div 
                        v-breadcrumbs( :items="items" large)
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader.text-h3 Custom divider
                    v-divider
                    div 
                        v-breadcrumbs( :items="items" divider="-")
                    div 
                        v-breadcrumbs( :items="items"  divider=">")
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader.text-h3 Icon Divider
                    v-divider
                    div 
                        v-breadcrumbs( :items="items")
                            template(v-slot:divider)
                                v-icon mdi-forward
                    div 
                        v-breadcrumbs( :items="items" )
                            template(v-slot:divider)
                                v-icon chevron_right
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader.text-h3 Item Slot
                    v-divider
                    div 
                        v-breadcrumbs( :items="items")
                            template( v-slot:item="{ item }")
                             v-breadcrumbs-item(:href="item.href" :disabled="item.disabled")  {{ item.text.toUpperCase() }}
        v-row
            v-col
                nuxt-link(to="/template"  nuxt) 
                    h3 Back to  Page Template
</template>
<script>
export default {
  layout: 'dropdownHeader',
  data() {
    return {
      items: [
        {
          text: 'Dashboard',
          disabled: false,
          href: 'breadcrumbs_dashboard',
        },
        {
          text: 'Link 1',
          disabled: false,
          href: 'breadcrumbs_link_1',
        },
        {
          text: 'Link 2',
          disabled: true,
          href: 'breadcrumbs_link_2',
        },
      ],
    }
  },
}
</script>
<style lang="scss" scoped>
// * {
//   border: 1px solid;
// }
// .main-content {
//   height: 500px;
// }
.bd-a {
  border: 1px solid lightgrey;
}
// .bd-x {
//   border-right: 1px solid;
//   border-left: 1px solid;
// }
</style>
