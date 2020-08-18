<template lang="pug">
    v-container
        v-row
            v-col
                h1 List Item Groups
                v-chip-group(column) 
                    v-chip(href="https://vuetifyjs.com/ja/components%20/list-item-groups/") v-list-item-group 
                    v-chip(href="https://vuetifyjs.com/ja/components%20/list-item-groups/") v-list-item  
                    v-chip(href="https://vuetifyjs.com/ja/components%20/list-item-groups/") v-list-item-action                        
                    v-chip(href="https://vuetifyjs.com/ja/components%20/list-item-groups/") v-list-item-avater                        
                    v-chip(href="https://vuetifyjs.com/ja/components%20/list-item-groups/") v-list-item-content                        
                    v-chip(href="https://vuetifyjs.com/ja/components%20/list-item-groups/") v-list-item-subtitle                        
                    v-chip(href="https://vuetifyjs.com/ja/components%20/list-item-groups/") v-list-item-action-text  
        //- v-row
        //-     v-col
        //-         h1 List 
        //-         v-chip-group(column) 
        //-             v-chip(href="https://vuetifyjs.com/ja/components/lists/") v-list 
        //-             v-chip(href="https://vuetifyjs.com/ja/components/lists/") v-list-item 
        //-             v-chip(href="https://vuetifyjs.com/ja/components/lists/") v-list-group
        //-             v-chip(href="https://vuetifyjs.com/ja/components/lists/") v-list-item-action
        //-             v-chip(href="https://vuetifyjs.com/ja/components/lists/") v-list-item-avater
        //-             v-chip(href="https://vuetifyjs.com/ja/components/lists/") v-list-item-content 
        v-row
            v-col(cols="12" md="12").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader.text-h3 Basic
                    v-divider
                    div.text-center
                    v-card.my-4.mx-auto(max-width="500")
                      v-list 
                        v-list-item-group(v-model="model") 
                          v-list-item(v-for="(item , i) in items" :key="i")   
                            v-list-item-icon  
                              v-icon {{item.icon}} 
                            v-list-item-content 
                              v-list-item-title 
                                span {{item.text}}
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader
                      span.text-h3 強調されていない選択
                    v-divider
                    div.text-center
                    v-card.my-4.mx-auto(max-width="500")
                      v-list(flat) 
                        v-list-item-group(v-model="model2" color="indigo") 
                          v-list-item(v-for="(item , ix2) in items2" :key="ix2")   
                            v-list-item-icon  
                              v-icon {{item.icon}} 
                            v-list-item-content 
                              v-list-item-title 
                                span {{item.text}}
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader
                      span.text-h3 複数のアイテムを選択
                    v-divider
                    div.text-center
                    v-card.my-4.mx-auto(max-width="500")
                      v-list 
                        v-list-item-group(v-model="model3" color="teal darken-1" multiple) 
                          v-list-item(v-for="(item , ix3) in items2" :key="ix3")   
                            v-list-item-icon  
                              v-icon {{item.icon}} 
                            v-list-item-content 
                              v-list-item-title 
                                span {{item.text}}
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader
                      span.text-h3 選択必須
                    v-divider
                    div.text-center
                    v-card.my-4.mx-auto(max-width="500")
                      v-list 
                        v-list-item-group(v-model="model4" color="purple darken-2" mandatory) 
                          v-list-item(v-for="(item , ix4) in items2" :key="ix4")   
                            v-list-item-icon  
                              v-icon {{item.icon}} 
                            v-list-item-content 
                              v-list-item-title 
                                span {{item.text}}
            v-col(cols="12" md="6").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader
                      span.text-h3 カスタムアクティブクラス
                    v-divider
                    div.text-center
                    v-card.my-4.mx-auto(max-width="500")
                      v-list 
                        v-list-item-group(v-model="model5" color="orange darken-2" active-class="border") 
                          v-list-item(v-for="(item , ix5) in items2" :key="ix5")   
                            v-list-item-icon  
                              v-icon {{item.icon}} 
                            v-list-item-content 
                              v-list-item-title 
                                span {{item.text}}
            v-col(cols="12" md="12").d-flex.flex-column.justify-start.align-start
                v-sheet(outlined rounded width="100%")
                    v-subheader
                      span.text-h3 選択コントロール
                    v-divider
                    div.text-center
                    v-card.my-4.mx-auto(max-width="500")
                      v-list(shaped)
                        v-subheader Selection controls
                        v-list-item-group(v-model="model6" multiple)
                          template(v-for="(item, ix6) in items6")
                            v-divider(v-if="!item" :key="`divider-${ix6}`") 
                            v-list-item(v-else :key="`item-${ix6}`" :value="item" )  
                              template(v-slot:default="{active}")
                                v-list-item-content
                                  v-list-item-title {{item}}
                                v-list-item-action 
                                  v-checkbox(:input-value="active")
                    v-card.my-4.mx-auto(max-width="500" flat)
                        span.text-h5 デフォルトのスロットを使用すると、アイテムの内部状態にアクセスして切り替えることができます。 activeプロパティはブール値なので、チェックボックスのtrue-valueプロパティを使用して、その状態をv-list-itemにリンクします。
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
        { icon: 'mdi-inbox', text: 'Inbox' },
        { icon: 'mdi-star', text: 'Star' },
        { icon: 'mdi-send', text: 'Send' },
        { icon: 'mdi-email-open', text: 'Drafts' },
      ],
      model: 0,
      items2: [
        { icon: 'mdi-wifi', text: 'Wifi' },
        { icon: 'mdi-bluetooth', text: 'Bluetooth' },
        { icon: 'mdi-chart-donut', text: 'Data Usage' },
      ],
      model2: 0,
      model3: 0,
      model4: 0,
      model5: 0,
      items6: ['Dog Photos', 'Cat Photos', '', 'Potatoes', 'Carrots'],
      model6: ['Carrots'],
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
.border {
  border: 2px dashed orange;
}
</style>
