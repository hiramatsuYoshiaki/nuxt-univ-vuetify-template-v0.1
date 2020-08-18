<template lang="pug">
    v-container
        v-row
            v-col
                h1 Menus
                v-chip-group(column) 
                    v-chip(href="https://vuetifyjs.com/ja/components/menus/") v-menu 
        v-row
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader.text-h3 Basic
                    v-divider
                    div.text-center.py-8
                        v-menu(offset-y)
                            template(v-slot:activator="{ on, attrs }")
                                v-btn( color="primary" dark v-bind="attrs" v-on="on") Dropdown 
                            v-list
                                v-list-item( v-for="(item, index) in items" :key="index" @click="" )
                                    v-list-item-title {{ item.title }}
                    v-card.my-4.px-4.mx-auto(max-width="500" flat)
                        span.text-h5 メニューをアクティブにする要素を activatorスロットに忘れずに配置してください。
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader.text-h3 ホバー
                    v-divider
                    div.text-center.py-8
                        v-menu(offset-y open-on-hover)
                            template(v-slot:activator="{ on, attrs }")
                                v-btn( color="primary" dark v-bind="attrs" v-on="on") Hover Dropdown 
                            v-list
                                v-list-item( v-for="(item, index) in items" :key="index" @click="" )
                                    v-list-item-title {{ item.title }}
            v-col(cols="12" md="12").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader.text-h3 カスタムトランジション
                    v-divider
                    div.py-8.d-flex.justify-space-around
                        v-menu(offset-y transition="scale-transition" bottom origin="center center")
                            template(v-slot:activator="{ on, attrs }")
                                v-btn( color="primary" dark v-bind="attrs" v-on="on" ) Scale 
                            v-list
                                v-list-item( v-for="(item, index) in items" :key="index" @click="" )
                                    v-list-item-title {{ item.title }}
                        v-menu(offset-y transition="slide-x-transition" bottom right)
                            template(v-slot:activator="{ on, attrs }")
                                v-btn( color="primary" dark v-bind="attrs" v-on="on" ) Slide X 
                            v-list
                                v-list-item( v-for="(item, index) in items" :key="index" @click="" )
                                    v-list-item-title {{ item.title }}
                        v-menu(offset-y transition="slide-y-transition" bottom)
                            template(v-slot:activator="{ on, attrs }")
                                v-btn( color="primary" dark v-bind="attrs" v-on="on" ) Slide Y 
                            v-list
                                v-list-item( v-for="(item, index) in items" :key="index" @click="" )
                                    v-list-item-title {{ item.title }}
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader.text-h3 横（X軸）方向へのオフセット
                    v-divider
                    div.py-8(class="text-center") 
                        v-switch(v-model="offsetX" label="X offset")
                        v-menu(bottom :offset-x="offsetX")
                            template(v-slot:activator="{ on, attrs }")
                                v-btn( color="primary" dark v-bind="attrs" v-on="on") Dropdown 
                            v-list
                                v-list-item( v-for="(item, index) in items" :key="index" @click="" )
                                    v-list-item-title {{ item.title }}
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader.text-h3 縦（Y軸）方向へのオフセット
                    v-divider
                    div.py-8(class="text-center") 
                        v-switch(v-model="offsetY" label="Y offset")
                        v-menu(bottom :offset-y="offsetY")
                            template(v-slot:activator="{ on, attrs }")
                                v-btn( color="primary" dark v-bind="attrs" v-on="on") Dropdown 
                            v-list
                                v-list-item( v-for="(item, index) in items" :key="index" @click="" )
                                    v-list-item-title {{ item.title }}
            v-col(cols="12" md="12").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader.text-h3 角丸
                    v-divider
                    div.py-8.d-flex.justify-space-around.align-center
                        v-menu(v-for="([text,rounded],ix6) in btns" :key="text" :rounded="rounded" offset-y)
                            template(v-slot:activator="{ on, attrs }")
                                v-btn.white--text.ma-8( :color="colors[ix6]" v-bind="attrs" v-on="on") {{text}} Radius- {{rounded}}
                            v-list
                                v-list-item( v-for="(item, index) in items" :key="index" @click="" )
                                    v-list-item-title {{ item.title }}
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader.text-h3 クリック時に閉じる
                    v-divider
                    div.py-8.text-center 
                        v-switch(v-model="closeOnClick" label="Close on click")
                        v-menu(bottom offset-y :close-on-click="closeOnClick") 
                            template(v-slot:activator="{on,attrs}")
                                v-btn(v-bind="attrs" v-on="on"  color="primary" dark) dropdown 
                            v-list 
                                v-list-item( v-for="(item, index) in items" :key="index" @click="" )
                                    v-list-item-title {{ item.title }}
                        v-card.my-4.px-4.mx-auto(max-width="500" flat)
                            span.text-h5 フォーカスが失ったときメニューを閉じることができます。
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader.text-h3 コンテンツのクリックで閉じる
                    v-divider
                    div.py-8.text-center 
                        v-switch(v-model="closeOnContentClick" label="Close on content click")
                        v-menu(bottom offset-y :close-on-content-click="closeOnContentClick") 
                            template(v-slot:activator="{on,attrs}")
                                v-btn(v-bind="attrs" v-on="on"  color="primary" dark) dropdown 
                            v-list 
                                v-list-item( v-for="(item, index) in items" :key="index" @click="" )
                                    v-list-item-title {{ item.title }}
                        v-card.my-4.px-4.mx-auto(max-width="500" flat)
                            span.text-h5 コンテンツがクリックされたときに v-menu を閉じるかどうかを設定することができます。
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader.text-h3 Absolute position
                    v-divider
                    div.py-8.d-flex.justify-center 
                        v-menu(v-model="showMenu" absolute offset-y style="max-width:600px")
                            template(v-slot:activator="{attrs,on}")
                                v-card(img="https://cdn.vuetifyjs.com/images/cards/girl.jpg"
                                        height="300"
                                        width="600"
                                        v-bind="attrs"
                                        v-on="on"
                                        class="portrait")
                            v-list 
                                v-list-item(v-for="(item,index7) in items" :key="index7")
                                    v-list-item-title {{item.title}}
            
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader.text-h3 Menus
                    v-divider
                    div.py-8.d-flex.justify-center 
                        v-card(height="200" min-width="500")
                            v-card-title.blue.white--text 
                                span.headline メニュー
                                v-spacer 
                                v-menu(bottom left) 
                                    template(v-slot:activator="{attrs,on}")
                                        v-btn(v-bind="attrs" v-on="on" dark  icon)
                                            v-icon mdi-dots-vertical 
                                    v-list 
                                        v-list-item(v-for="(item,index8) in items" :key="index8")
                                            v-list-item-title {{item.title}}
                            v-card-text.pa-4 Lorem Ipsum
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader.text-h3 ポップオーバーメニュー
                    v-divider
                    div.py-8.d-flex.justify-center 
                       v-menu(v-model="menu" :close-on-content-click="false"  :nudge-width="200" offset-x)
                        template(v-slot:activator="{attrs,on}")
                            v-btn(color="indigo" dark v-bind="attrs" v-on="on") Menu as Popover
                        v-card 
                            v-list 
                                v-list-item 
                                    v-list-item-avatar 
                                        img(src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John")
                                    v-list-iten-content 
                                        v-list-item-title John Leider 
                                        v-list-item-subtitle Founder of Vuetify.js 
                                    v-spacer
                                    v-list-item-action 
                                        v-btn(:class="fav ? 'red--text' : ''" icon @click="fav= !fav")
                                            v-icon mdi-heart
                            v-divider
                            v-list 
                                v-list-item 
                                    v-list-item-action 
                                        v-switch(v-model="message" color="purple")
                                    v-list-item-title Enable message 
                                v-list-item 
                                    v-list-item-action 
                                        v-switch(v-model="hints" color="purple")
                                    v-list-item-title Enable hints
                            v-card-actions 
                                v-spacer 
                                v-btn(text  @click="menu = false") Cansel 
                                v-btn(text color="primary" @click="menu = false") Save

        v-row
            v-col
                nuxt-link(to="/template"  nuxt) 
                    h3.mb-16 Back to  Page Template
                   
</template>
<script>
export default {
  layout: 'dropdownHeader',
  data() {
    return {
      items: [
        { title: 'Click Me' },
        { title: 'Click Me' },
        { title: 'Click Me' },
        { title: 'Click Me 2' },
      ],
      offsetY: true,
      offsetX: true,
      btns: [
        ['Removed', '0'],
        ['Large', 'lg'],
        ['Custom', 'b-xl'],
      ],
      colors: ['deep-purple accent-4', 'error', 'teal darken-1'],
      items2: [[...Array(4)].map((_, i) => `Item ${i}`)],
      closeOnClick: true,
      closeOnContentClick: true,
      showMenu: false,
      fav: true,
      menu: false,
      message: false,
      hints: true,
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
