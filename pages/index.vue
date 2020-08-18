<template lang="pug">
 v-container
        //- v-row
        //-     v-col
        //-         div
        //-         v-breadcrumbs( :items="items" large)
        //- v-row
        //-     v-col
                h1 Nuxt  Vuetify Start Template V0.2
        //- v-row
        //-     v-col
        //-         nuxt-link(to="/"  nuxt) 
        //-             h3 Back to  Nuxt HOME
        v-row 
          v-col   
            h1 Nuxt  Vuetify Start Template V0.2
        div  
          h1 スタートテンプレートを使う準備
        v-row 
         v-col 
          h3 1.Start 
            h4 GitHub リポジトリを clone してローカルプロジェクト作る
        div  
          h1 スタートテンプレートの設定内容
        v-row 
          v-col 
            h3 2.Customs
        v-row 
          v-col 
            h3 3.Styles
             h4 SASS変数を使う
             h4 styles.scssを使う
             h4 fundationを設定する
             h4 フォントサイズを設定する
        div  
          h1 スタートテンプレートの説明
        v-row 
          v-col  
           h4 4.Layouts
            h4 ｎｕｘｔのｌａｙｏｕｔを設定する
            h4 テンプレートの種類
          

              //- pre 
              //-   code 
              //-     div.heml-grp 
              //-       h5 &lt; template lang="pug" &gt;
              //-       h5     div.cardLayout
              //-       h5       div.cardLayout-card
              //-       h5         div.element element
              //-       h5     //- Repeap other card total 10 card
              //-       h5 &lt; /template &gt;
              //-     div.css-grp
              //-       h5 &lt; style lang="scss" scoped &gt;
              //-       h5      .cardLayout {
              //-       h5.orenge        display: flex;
              //-       h5.orenge        flex-wrap: wrap;
              //-       h5        margin: 0;
              //-       h5        padding: 0;
              //-       h5        width: 100%;;
              //-       h5        height: 100%;
              //-       h5      }
              //-       h5      .cardLayout-card {
              //-       h5       // There will be 4 cards per row
              //-       h5        flex-basis: 25%;
              //-       h5        height: 25%;
              //-       h5        padding: 40px;
              //-       h5        background-color: rgba(0, 0, 0, 0.3);
              //-       h5        border: 1px dotted rgba(0, 0, 0, 0.2);
              //-       h5      }
              //-       h5      .element {
              //-       h5         width: 100%;
              //-       h5         height: 100%;
              //-       h5         border-radius: 2px;
              //-       h5         background-color: rgba(0, 0, 0, 0.5);
              //-       h5         color: $white;
              //-       h5      }
              //-       h5 &lt; /style &gt;
</template>

<script>
export default {
  layout: 'sidebarNav-vuetify',
}
</script>
<style lang="scss" scoped>
.heml-grp {
  color: yellow;
}
.css-grp {
  color: green;
}
.blue {
  color: blue;
}
.orenge {
  color: orange;
}
.red {
  color: red;
}
</style>
