<template lang="pug">
        v-container(fluid class="grey lighten-5")
            v-row
                v-col(cols="12" )
                    v-card.ps-2(outline tile )
                        h1 Layout Shifter (Grid System by Flexbox)
                        h3 Components/Grid
                        h3 v-container
                        nuxt-link(to="/respPattern") 
                            h3 back to Nuxt Responsive Pattern
                v-col(cols="12" )
                    v-card.ps-2(outline tile )
                        h1 xs -600px col12
                        h1 sm 600px-960px col12
                        h1 md 960px-1264px col12
                        h1 lg 1264px-1904px col12
                        h1 xl 1904- col12
            v-row(justify="space-around" aling="center")
                v-col( cols="12" lg="4")
                    //- div.title.mb-1 Default (cover)
                    div.subheading Matching
                    v-img( src="https://picsum.photos/510/300?random" aspect-ratio="1.7")
                v-col( cols="12" lg="4")
                    div.subheading.pt-4 Too high
                    v-img( src="https://picsum.photos/510/300?random" aspect-ratio="2")
                v-col( cols="12" lg="4")
                    div.subheading.pt-4 Too low
                    v-img( src="https://picsum.photos/510/300?random" aspect-ratio="1.4")
                       

</template>
<script>
export default {
  layout: 'fullscreenNav',
}
</script>
<style lang="scss" scoped>
$size-1: 5rem !default;
$size-2: 4rem !default;
$size-3: 3rem !default;
$size-4: 2rem !default;
$size-5: 1.5rem !default;
$size-6: 1rem !default;
$size-7: 0.75rem !default;
$size-8: 0.5rem !default;
$mobile: 0.8; //768
$tablet: 1; //769
$desktop: 1.2; //960
$widescreen: 1.5; //1152
$fullhd: 1.7; //1344
h1,
.h1 {
  font-size: $size-1;
  font-weight: 400;
  line-height: 1.5;
}

h2,
.h2 {
  font-size: $size-2;
  font-weight: 400;
  line-height: 1.5;
}

h3,
.h3 {
  font-size: $size-3;
  font-weight: 400;
  line-height: 1.5;
}

h4,
.h4 {
  font-size: $size-4;
  font-weight: 400;
  line-height: 1.5;
}

h5,
.h5 {
  font-size: $size-5;
  font-weight: 400;
  line-height: 1.5;
}
h6,
.h6 {
  font-size: $size-6;
  font-weight: 400;
  line-height: 1.5;
}

p {
  font-size: $size-5;
  font-weight: 500;
  line-height: 1.5;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
h5,
.h6 {
  font-weight: 300;
}
p,
.p {
  font-weight: 500;
}

/* Responsive Headings */

@media (max-width: 768px) {
  h1,
  .h1 {
    font-size: calc(#{$mobile} * #{$size-1});
    font-weight: 400;
    line-height: 1.5;
  }
  h2,
  .h2 {
    font-size: calc(#{$mobile} * #{$size-2});
    font-weight: 400;
    line-height: 1.5;
  }
  h3,
  .h3 {
    font-size: calc(#{$mobile} * #{$size-3});
    font-weight: 400;
    line-height: 1.5;
  }
  h4,
  .h4 {
    font-size: calc(#{$mobile} * #{$size-4});
    font-weight: 400;
    line-height: 1.5;
  }
  h5,
  .h5 {
    font-size: calc(#{$mobile} * #{$size-5});
    font-weight: 400;
    line-height: 1.5;
  }
  h6,
  .h6 {
    font-size: calc(#{$mobile} * #{$size-6});
    font-weight: 400;
    line-height: 1.5;
  }
  p,
  .p {
    font-size: calc(#{$mobile} * #{$size-5});
    font-weight: 500;
    line-height: 1.5;
  }
}
/* Small Devices, Tablets */
// 769/960/1152/1344

@media (min-width: 960px) {
  h1,
  .h1 {
    font-size: calc(#{$desktop} * #{$size-1});
    font-weight: 400;
    line-height: 1.5;
  }
  h2,
  .h2 {
    font-size: calc(#{$desktop} * #{$size-2});
    font-weight: 400;
    line-height: 1.5;
  }
  h3,
  .h3 {
    font-size: calc(#{$desktop} * #{$size-3});
    font-weight: 400;
    line-height: 1.5;
  }
  h4,
  .h4 {
    font-size: calc(#{$desktop} * #{$size-4});
    font-weight: 400;
    line-height: 1.5;
  }
  h5,
  .h5 {
    font-size: calc(#{$desktop} * #{$size-5});
    font-weight: 400;
    line-height: 1.5;
  }
  h6,
  .h6 {
    font-size: calc(#{$desktop} * #{$size-6});
    font-weight: 400;
    line-height: 1.5;
  }
  p,
  .p {
    font-size: calc(#{$desktop} * #{$size-5});
    font-weight: 500;
    line-height: 1.5;
  }
}
@media (min-width: 1152px) {
  h1,
  .h1 {
    font-size: calc(#{$widescreen} * #{$size-1});
    font-weight: 400;
    line-height: 1.5;
  }
  h2,
  .h2 {
    font-size: calc(#{$widescreen} * #{$size-2});
    font-weight: 400;
    line-height: 1.5;
  }
  h3,
  .h3 {
    font-size: calc(#{$widescreen} * #{$size-3});
    font-weight: 400;
    line-height: 1.5;
  }
  h4,
  .h4 {
    font-size: calc(#{$widescreen} * #{$size-4});
    font-weight: 400;
    line-height: 1.5;
  }
  h5,
  .h5 {
    font-size: calc(#{$widescreen} * #{$size-5});
    font-weight: 400;
    line-height: 1.5;
  }
  h6,
  .h6 {
    font-size: calc(#{$widescreen} * #{$size-6});
    font-weight: 400;
    line-height: 1.5;
  }
  p,
  .p {
    font-size: calc(#{$widescreen} * #{$size-5});
    font-weight: 500;
    line-height: 1.5;
  }
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
h5,
.h6,
p,
.p {
  margin: 0;
  padding: 0;
}
</style>
