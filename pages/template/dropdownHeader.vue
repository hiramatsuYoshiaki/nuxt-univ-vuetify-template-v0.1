<template lang="pug">
    v-container
        v-row
            v-col
                h1 DropdownHeader
                h3 Components/Application
                h3 v-scroll-y-transition
        v-row
            v-col
                nuxt-link(to="/appLayout"  nuxt) 
                    h3 Back to  App Layout
</template>
<script>
export default {
  layout: 'dropdownHeader',
}
</script>
<style lang="scss" scoped>
// * {
//   border: 1px solid;
// }
</style>
