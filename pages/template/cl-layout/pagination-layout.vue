<template lang="pug">
    v-container
        v-row
            v-col
                h1 pagination
                v-chip-group(column) 
                    v-chip(href="https://vuetifyjs.com/ja/components/paginations/") v-pagination 
        v-row
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader.text-h3 Basic
                    v-divider
                    div.text-center.py-4
                        v-pagination(v-model="page_value1" :length="6")
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader.text-h3 Logn
                    v-divider
                    div.text-center.py-4
                            v-pagination(v-model="page_value2" :length="15" )
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader.text-h3 Limit
                    v-divider
                    div.text-center.py-4
                            v-pagination(v-model="page_value3" :length="15" :total-visible="7")
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader.text-h3 Circle
                    v-divider
                    div.text-center.py-4
                            v-pagination(v-model="page_value4" :length="4" circle)
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader.text-h3 Previus Next Icon
                    v-divider
                    div.text-center.py-4
                            v-pagination(v-model="page_value5" :length="4" prev-icon="mdi-menu-left"  next-icon="mdi-menu-right")
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader.text-h3 Disabled
                    v-divider
                    div.text-center.py-4
                            v-pagination(v-model="page_value6" :length="4" disabled)
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
      page_value1: 1,
      page_value2: 1,
      page_value3: 1,
      page_value4: 1,
      page_value5: 1,
      page_value6: 1,
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
