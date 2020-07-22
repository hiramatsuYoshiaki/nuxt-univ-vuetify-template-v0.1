<template lang="pug">
        v-container
            v-row
                v-col
                    h1 Nuxt Responsive Pattern
            v-row
                v-col
                    nuxt-link(to="/respPattern/mostlyFluid") 
                        h1  MostlyFluid 
            v-row
                v-col
                    nuxt-link(to="/respPattern/columnDrop") 
                        h1  Column drop 
            v-row
                v-col
                    nuxt-link(to="/respPattern/layoutShifter") 
                        h1  Layout shifter
            v-row
                v-col
                    nuxt-link(to="/respPattern/tinyTweaks") 
                        h1  Tiny tweaks 
            v-row
                v-col
                    nuxt-link(to="/respPattern/offCanvas") 
                        h1  Off canvas 
</template>
<script>
export default {
  layout: 'baseline',
}
</script>
<style lang="scss" scoped>
// * {
//   border: 1px solid;
// }
</style>
