<template lang="pug">
    v-container.columns
        v-row
            v-col
                h1 Mostly Fluid (Grid System by Flexbox)
                h3 Components/Grid
                h3 v-container
        v-row
            v-col
                nuxt-link(to="/respPattern") 
                    h3 back to Nuxt Responsive Pattern
</template>
<script>
export default {
  layout: 'fullscreenNav',
}
</script>
<style lang="scss" scoped>
.columns {
  border: 1px solid grey;
}
</style>
