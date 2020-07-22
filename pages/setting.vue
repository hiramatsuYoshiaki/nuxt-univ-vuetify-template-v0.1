<template lang="pug">
    v-container
        v-row
            v-col
                div.text-h1 Check the style
        v-row
            v-col
                h1 Text And Typography
                h3 Control text size, alignment, wrapping, overflow, transforms and more.
        v-row
            v-col(cols="12")
                v-item-group(mandatory) 
                    v-sheet(max-height="600" tile  class="overflow-y-auto" elevation="6")
                        v-item(v-for="[c,text,size,weight,spacing,margin] in classes" :key="c")
                            template(v-slot="{active, toggle}") 
                                v-sheet(
                                    :color="active ? 'grey lighte-4' : undefined"
                                    class="px-4 pt-4 pb-3"
                                    tile 
                                    style="cursor: pointer"
                                    @click="toggle"
                                    )
                                    div(
                                        :class="[`text-${c}`,active && `mb-${margin}`]"
                                        class="transition-swing"
                                        v-text="text"
                                        ) 
                                    v-expand-transition 
                                        v-responsive(v-if="active" max-width="350")
                                            div(class="d-flex justify-space-between caption").mt-3 
                                                div
                                                    div(class="mb-2 white--text") Font
                                                    div(class="font-weight-medium") Roboto
                                                div 
                                                    div(class="mb-2 white--text") Weight
                                                    div(class="font-weight-medium" v-text="weight")
                                                div 
                                                    div(class="mb-2 white--text") Size
                                                    div(class="font-weight-medium" v-text="size")
                                                div 
                                                    div(class="mb-2 white--text") Letter spacing
                                                    div(class="font-weight-medium" v-text="spacing") 
                                               
        v-row 
            v-col(cols="12") 
                div.text-h1 Font size on Responsive
                v-item-group.pa-2.d-flex.justify-center(v-model="modelCaption" mandatory) 
                    v-item(v-for="([icon,bp,size],i) in sizes"  :key="i" :value="size")  
                        template(v-slot="{active,toggle}")
                           v-hover(v-slot:default="{hover}")
                                div.ma-3.text-center(
                                    :class="[(active||hover) ? 'text--primary' : 'text--secondary', hover ? 'elevation-1' : '' ]"
                                    style="cursor: pointer"
                                    @click="toggle"
                                    )
                                        v-icon.pa-1.mb-1(:color="(active || hover) ? 'grey darken-4' : 'grey lighten-1'") {{ icon}}
                                        div.caption {{ bp}} 
                div.text-h5.mb-6.text-center 
                    code {{typeClass}} 
                v-card(
                    class="d-flex align-center justify-center pa-4 mx-auto"
                    max-width="550"
                    min-height="76"
                    outlined
                )
                    div(:class="`text-${modelCaption}`") Example Heading-{{modelCaption}}

        v-row
            v-col(cols="12")
                div1
                    div.text-h1.my-2 FONT SIZE Vuetify
                    div.text-h1.my-2 text-h1
                    div.text-h2.my-2 text-h2
                    div.text-h3.my-2 text-h3
                    div.text-h4.my-2 text-h4
                    div.text-h5.my-2 text-h5
                    div.text-h6.my-2 text-h6
                    div.text-subtitle-1.my-2 subtitle-1
                    div.text-subtitle-2.my-2 subtitle-2
                    div.text-body-1.my-2 body-1
                    div.text-body-2.my-2 body-2
                    div.text-button.my-2 button
                    div.text-caption.my-2 caption
                    div.text-overline.my-2 overline
                   
                    hr
                    h1 font-size: 62.5%;
                    div.rem size 1.6rem = 16px
                    div.pxs size 16px = 1.6rem
                    div.em size 1.6em = 16px
                    div.rem-box 
                        p 10rem box 
                    div.px-box 
                        p 100px box
                    hr
                //- div
                //-     h1 FONT SIZE default
                //-     h1 見出し１ Heading1 h1
                //-     h2 見出し２ Heading2 h2
                //-     h3 見出し３ Heading3 h3
                //-     h4 見出し４ Heading4 h4
                //-     h5 見出し５ Heading5 h5
                //-     h6 見出し６ Heading6 <h6></h6>
                //-     div.h7 見出し７ Heading7 div.h7
                //-     p 見出しP p
                //-     hr
                //-     h1 font-size: 62.5%;
                //-     div.rem size 1.6rem = 16px
                //-     div.pxs size 16px = 1.6rem
                //-     div.em size 1.6em = 16px
                //-     div.rem-box 
                //-         p 10rem box 
                //-     div.px-box 
                //-         p 100px box
               
  
</template>
<script>
export default {
  layout: 'baseline',
  data() {
    return {
      model: null,
      classes: [
        ['h1', 'Heading 1', '6rem', '300', '-0.09375rem', -1],
        ['h2', 'Heading 2', '3.75rem', '300', '-0.03125rem', 0],
        ['h3', 'Heading 3', '3rem', '400', 'normal', 1],
        ['h4', 'Heading 4', '2.125rem', '400', '0.015625rem', 2],
        ['h5', 'Heading 5', '1.5rem', '400', 'normal', 2],
        ['h6', 'Heading 6', '1.25rem', '500', '0.009375rem', 3],
        ['subtitle-1', 'Subtitle 1', '1rem', '400', '0.009375rem', 4],
        ['subtitle-2', 'Subtitle 2', '0.875rem', '500', '0.00625rem', 4],
        ['body-1', 'Body 1', '1rem', '400', '0.03125rem', 4],
        ['body-2', 'Body 2', '0.875rem', '400', '0.015625rem', 4],
        ['button', 'Button', '0.875rem', '500', '0.078125rem', 4],
        ['caption', 'Caption', '0.75rem', '400', '0.025rem', 4],
        ['overline', 'Overline', '0.75rem', '500', '0.1666666667em', 4],
      ],
      modelCaption: 'caption',
      sizes: [
        ['mdi-devices', 'all', 'caption'],
        ['mdi-cellphone-iphone', 'sm', 'body-2'],
        ['mdi-laptop', 'md', 'body-1'],
        ['mdi-monitor', 'lg', 'h6'],
        ['mdi-television', 'xl', 'h4'],
      ],
    }
  },
  computed: {
    typeClass() {
      const type = ['text', this.modelCaption]
      const [, breakpoint] = this.current
      if (breakpoint !== 'all') {
        type.splice(1, 0, breakpoint)
      }
      return `.${type.join('-')}`
    },
    current() {
      return this.sizes.find((size) => size[2] === this.modelCaption)
    },
  },
}
</script>
<style lang="scss" scoped>
.rem10 {
  font-size: 10rem;
  color: blue;
}
.px100 {
  font-size: 100px;
  color: red;
}
.rem-box {
  font-size: 10rem;
  width: 50rem;
  height: 20rem;
  background-color: blue;
}
.px-box {
  font-size: 100px;
  width: 500px;
  height: 200px;
  background-color: red;
}
.rem {
  font-size: 1.6rem;
  color: blue;
}
.pxs {
  font-size: 16px;
  color: red;
}
.em {
  font-size: 1.6em;
  color: purple;
}
</style>
