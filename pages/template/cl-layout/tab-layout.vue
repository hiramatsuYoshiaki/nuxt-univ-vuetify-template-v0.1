<template lang="pug">
    v-container
        v-row
            v-col
                h1 Tabs
                v-chip-group(column) 
                    v-chip(href="https://vuetifyjs.com/ja/components/tabs/") v-tabs 
                    v-chip(href="https://vuetifyjs.com/ja/components/tabs/") v-item 
                    v-chip(href="https://vuetifyjs.com/ja/components/tabs/") v-items 
                    v-chip(href="https://vuetifyjs.com/ja/components/tabs/") v-slider 
        v-row
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%").px-4
                    v-subheader.text-h3 Basic
                    v-divider
                    div.text-center.py-4
                        v-tabs
                            v-tab Item One
                            v-tab Item Two
                            v-tab Item Three
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%").px-4
                    v-subheader
                        span.text-h3.mr-4  Fixed 
                        span.text-h5 最大幅 (300px) 
                    v-divider
                    div.text-center.py-4
                        v-tabs(fixed-tabs background-color="indigo" dark)
                            v-tab Option
                            v-tab Another Selection
                            v-tab Items
                            v-tab Another Screen
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%").px-4
                    v-subheader
                        span.text-h3.mr-4  Centered active
                        span.text-h5 Active tab is always centered
                    v-divider
                    div.text-center.py-4
                        v-tabs(center-active background-color="deep-purple accent-4" dark)
                            v-tab One
                            v-tab Two
                            v-tab Three
                            v-tab Four
                            v-tab Five
                            v-tab Six
                            v-tab Seven
                            v-tab Eight
                            v-tab Nine
                            v-tab Ten
                            v-tab Eleven
                            v-tab Twelve
                            v-tab Thirteen
                            v-tab Fourteen
                            v-tab Fifteen
                            v-tab Sixteen
                            v-tab Seventeen
                            v-tab Eighteen
                            v-tab Nineteen
                            v-tab Twenty
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%").px-4
                    v-subheader
                        span.text-h3.mr-4  Tab Items
                        span.text-h5 Active tab is always centered
                    v-divider
                    div.text-center.py-4
                        v-tabs(v-model="tab_1" center-active background-color="primary" dark)
                            v-tab(v-for="item in items_1" :key="item.tab") {{ item.tab }}
                        v-tabs-items(v-model="tab_1")
                            v-tab-item(v-for="item in items_1" :key="item.tab")
                                v-card(outlined)
                                        v-card-text {{ item.content }}
            
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%").px-4
                    v-subheader
                        span.text-h3.mr-4  ページネーション
                        span.text-h5 show arrows
                    v-divider
                    v-card.text-center.py-4.mb-4
                        v-tabs(dark  background-color="teal darken-3"  show-arrows)
                                v-tabs-slider color="teal lighten-3"
                                v-tab( v-for="i in 30" :key="i" :href="'#tab-' + i") Item {{ i }}
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%").px-4
                    v-subheader
                        span.text-h3.mr-4  カスタムアイコン
                        span.text-h5 prev-icon next-icon
                    v-divider
                    v-card.text-center.py-4.mb-4
                        v-tabs(dark  background-color="cyan"  
                                show-arrows next-icon="mdi-arrow-right-bold-box-outline"
                                prev-icon="mdi-arrow-left-bold-box-outline")
                                v-tabs-slider color="teal lighten-3"
                                v-tab( v-for="i in 30" :key="i" :href="'#tab-' + i") Item {{ i }}
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%").px-4
                    v-subheader
                        span.text-h3.mr-4  Grow
                        span.text-h5 show-arrows
                    v-divider
                    v-card.text-center.py-4.mb-4.basil
                        v-card-title.text-center.justify-center.py-6 
                            h3.text-h3.font-weight-bold.display-3.basil--text BASiL
                        v-tabs(v-model="tab_2" grow background-color="transparent"  color="basil")
                            v-tab(v-for="item2 in items_2" :key="item2") {{ item2 }}
                        v-tabs-items(v-model="tab_2")
                            v-tab-item(v-for="item2 in items_2" :key="item2")
                                v-card(outlined color="basil")
                                        v-card-text {{ text_2}}
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%").px-4
                    v-subheader
                        span.text-h3.mr-4  Vertical Tabs
                        span.text-h5 prev-icon next-icon
                    v-divider
                    v-card.text-center.py-4.mb-4
                        v-tool-br(flat background="primary" dark )
                            v-toolbar-title user profile
                        v-tabs(vertical)
                            v-tab
                                v-icon(left) mdi-account 
                                    span Option 1
                            v-tab
                                v-icon(left) mdi-lock 
                                    span Option 2
                            v-tab
                                v-icon(left) mdi-access-point 
                                    span Option 3
                            v-tab-item
                                v-card(flat)
                                    v-card-text 
                                        p Sed aliquam ultrices mauris. Donec posuere vulputate arcu. Morbi ac felis. Etiam feugiat lorem non metus. Sed a libero.
                                        p Nam ipsum risus, rutrum vitae, vestibulum eu, molestie vel, lacus. Aenean tellus metus, bibendum sed, posuere ac, mattis non, nunc. Aliquam lobortis. Aliquam lobortis. Suspendisse non nisl sit amet velit hendrerit rutrum.
                                        p( class="mb-0") Phasellus dolor. Fusce neque. Fusce fermentum odio nec arcu. Pellentesque libero tortor, tincidunt et, tincidunt eget, semper nec, quam. Phasellus blandit leo ut odio.
                            v-tab-item
                                v-card(flat)
                                    v-card-text 
                                        p Morbi nec metus. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante convallis tellus, vitae iaculis lacus elit id tortor. Sed mollis, eros et ultrices tempus, mauris ipsum aliquam libero, non adipiscing dolor urna a orci. Curabitur ligula sapien, tincidunt non, euismod vitae, posuere imperdiet, leo. Nunc sed turpis.
                            v-tab-item
                                v-card(flat)
                                    v-card-text 
                                        p Fusce a quam. Phasellus nec sem in justo pellentesque facilisis. Nam eget dui. Proin viverra, ligula sit amet ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. In dui magna, posuere eget, vestibulum et, tempor auctor, justo.
                                       
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%").px-4
                    v-subheader
                        span.text-h3.mr-4  TEXT ICON
                        span.text-h5 Include Icons
                    v-divider
                    v-card.text-center.py-4.mb-4
                        v-tabs( v-model="tab_3"
                                background-color="deep-purple accent-4"  
                                centered
                                dark
                                icons-and-text)
                            v-tabs-slider 
                            v-tab( href="#tab-1") 
                                span Recents
                                v-icon mdi-phone
                            v-tab( href="#tab-2") 
                                span Favorites
                                v-icon mdi-heart
                            v-tab( href="#tab-3") 
                                span Nearby
                                v-icon mdi-account-box
                        v-tabs-items(v-model="tab_3") 
                            v-tab-item( v-for="i in 3" :key="i" :value="'tab-' + i")
                                v-card(outlined)
                                    v-card-text {{ text_2 }}
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%").px-4
                    v-subheader
                        span.text-h3.mr-4  Right aligned tabs
                        //- span.text-h5 Include Icons
                    v-divider
                    v-card.text-center.py-4.mb-4
                        v-tabs( background-color="white"  
                                color="deep-purple accent-4"
                                right)
                            v-tab Landscape
                            v-tab City
                            v-tab Abstract
                            v-tab-item(v-for="n in 3" :key="n")
                                v-container
                                    v-row 
                                        v-col(v-for="i in 8" :key="i" col="12" md="3") 
                                            //- v-card(outlined)
                                            //-     v-card-text 
                                            //-         h1 tab item - {{ n }}
                                            v-img(
                                                 :src="`https://picsum.photos/200/150?image=${i * n * 5 + 10}`"
                                                 :lazy-src="`https://picsum.photos/10/6?image=${i * n * 5 + 10}`"
                                                 aspect-ratio="1"
                                             )

                            //-             v-col(v-for="i in 6" :key="i" col="12" md="3")
                            //-                 v-img(
                            //-                     :src="`https://picsum.photos/500/300?image=${i * n * 5 + 10}`"
                            //-                     :lazy-src="`https://picsum.photos/10/6?image=${i * n * 5 + 10}`"
                            //-                     aspect-ratio="1"
                            //-                 )

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
      tab_1: null,
      items_1: [
        { tab: 'One', content: 'Tab 1 Content' },
        { tab: 'Two', content: 'Tab 2 Content' },
        { tab: 'Three', content: 'Tab 3 Content' },
        { tab: 'Four', content: 'Tab 4 Content' },
        { tab: 'Five', content: 'Tab 5 Content' },
        { tab: 'Six', content: 'Tab 6 Content' },
        { tab: 'Seven', content: 'Tab 7 Content' },
        { tab: 'Eight', content: 'Tab 8 Content' },
        { tab: 'Nine', content: 'Tab 9 Content' },
        { tab: 'Ten', content: 'Tab 10 Content' },
      ],
      tab_2: null,
      items_2: ['Appetizers', 'Entrees', 'Deserts', 'Cocktails'],
      text_2:
        'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
      tab_3: null,
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
.basil {
  background-color: #fffbe6 !important;
}
.basil--text {
  color: #356859 !important;
}
</style>
