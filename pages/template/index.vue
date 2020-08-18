<template lang="pug">
v-container(fluid)
    v-row 
        v-col(cols="12")
            div.text-h1.mb-4 Page Template
            //- v-btn.text-h3.pa-4(href="https://developers.google.com/web/fundamentals/design-and-ux/responsive/patterns?hl=ja")  レスポンシブ ウェブデザイン パターン 
            v-btn(@click="isOpenResponsivePattern=!isOpenResponsivePattern")
                span.text-h3.mr-2  レスポンシブ ウェブデザイン パターン
                v-icon(v-show="!isOpenResponsivePattern") fas fa-angle-down
                v-icon(v-show="isOpenResponsivePattern") fas fa-angle-up
    v-row(v-show="isOpenResponsivePattern") 
        v-col(cols="12" sm="12" md="12" lg="6")
            v-sheet(class="pa-12" color="grey lighten-3" )
                nuxt-link(to="respPattern/mostlyFluid")
                    h1.mb-4 Mostly Fluid
                    h4 ほとんどの fluid パターンは、主に fluid グリッドで構成されています。一般的に、大画面または中画面ではサイズを保ち、より広い画面上では余白の調整のみを行います。
                    h4 小さな画面の場合、fluid グリッドではメインコンテンツのリフローが発生し、列が垂直方向にスタックされます。 このパターンの主な利点の 1 つは、 通常、小画面と大画面の間に 1 つの ブレークポイントだけが必要であることです。
                div.layout-grp
                    div.layout-element.layout-wrape-xs 
                        div.c1.xs-c1
                        div.c2.xs-c2
                        div.c3.xs-c3
                        div.c4.xs-c4
                        div.c5.xs-c5
                        div.subscription 
                            h1 xs 
                            h5 -600
                            h6 handset
                    div.layout-element.layout-wrape-sm  
                        div.c1.sm-c1
                        div.d-flex
                            div.c2.sm-c2
                            div.c3.sm-c3
                        div.d-flex
                            div.c4.sm-c4
                            div.c5.sm-c5
                        div.subscription 
                            h1 sm 
                            h5 600-960
                            h6 tablet
                    div.layout-element.layout-wrape-md 
                        div.c1.md-c1
                        div.d-flex
                            div.c2.md-c2
                            div.c3.md-c3
                        div.d-flex
                            div.c4.md-c4
                            div.c5.md-c5
                        div.subscription 
                            h1 md 
                            h5 960-1264
                            h6 tablet
                            h6 laptop
                    div.layout-element.layout-wrape-lg 
                        div.d-flex 
                            div.c1.lg-c1
                            div.c2.lg-c2
                        div.d-flex
                            div.c3.lg-c3
                            div.c4.lg-c4
                            div.c5.lg-c5
                        div.subscription 
                            h1 lg 
                            h5 1264-1904 
                            h6 desktop
                    div.layout-element.layout-wrape-xl 
                        div.d-flex 
                            div.c1.xl-c1
                            div.c2.xl-c2
                        div.d-flex
                            div.c3.xl-c3
                            div.c4.xl-c4
                            div.c5.xl-c5
                        div.subscription 
                            h1 xl
                            h5 1904-
                            h6 4k
                            h6 ultra-wides
        v-col(cols="12" sm="12" md="12" lg="6")
            v-sheet(class="pa-12" color="grey lighten-3" )
                nuxt-link(to="respPattern/columnDrop")
                    h1.mb-4 Column drop 
                    h4 Column drop は幅いっぱいに表示するマルチカラム レイアウトです。コンテンツに対してウィンドウ幅が狭くなると、単純に列を垂直にスタックします。
                    h4 最終的には、すべての列が垂直にスタックされます。このレイアウト パターンでは、コンテンツやデザインの変化に合わせてブレークポイントを指定します。
                div.layout-grp
                    div.layout-element.layout-wrape-xs 
                        div.c1.xs-cd-c1
                        div.c2.xs-cd-c2
                        div.c3.xs-cd-c3
                        div.subscription 
                            h1 xs 
                            h5 -600
                            h6 handset
                    div.layout-element.layout-wrape-sm  
                        div.c1.sm-cd-c1
                        div.c2.sm-cd-c2
                        div.c3.sm-cd-c3
                        div.subscription 
                            h1 sm 
                            h5 600-960
                            h6 tablet
                    div.layout-element.layout-wrape-md 
                        div.d-flex
                            div.c1.md-cd-c1
                            div.c2.md-cd-c2
                        div.d-flex
                            div.c3.md-cd-c3
                        div.subscription 
                            h1 md 
                            h5 960-1264
                            h6 tablet
                            h6 laptop
                    div.layout-element.layout-wrape-lg 
                        div.d-flex 
                            div.c1.lg-cd-c1
                            div.c2.lg-cd-c2
                            div.c3.lg-cd-c3
                        div.subscription 
                            h1 lg 
                            h5 1264-1904 
                            h6 desktop
                    div.layout-element.layout-wrape-xl 
                        div.d-flex 
                            div.c1.xl-cd-c1
                            div.c2.xl-cd-c2
                            div.c3.xl-cd-c3
                        div.subscription 
                            h1 xl
                            h5 1904-
                            h6 4k
                            h6 ultra-wides
        v-col(cols="12" sm="12" md="12" lg="6")
            v-sheet(class="pa-12" color="grey lighten-3" )
                nuxt-link(to="respPattern/layoutShifter")
                    h1.mb-4 Layout shifter 
                    h4 Layout shifter パターンは最もレスポンシブなパターンで、さまざまな画面幅に合わせて複数のブレークポイントを設定します。
                    h4 このレイアウトの鍵は、リフローや他の列の下へのドロップではなく、コンテンツの移動です。 各主要ブレイクポイント間の大きな差によって、維持が複雑になり、 全体的なコンテンツのレイアウトだけでなく、要素内の変化が 含まれる可能性があります。
                div.layout-grp
                    div.layout-element.layout-wrape-xs 
                        div.c1.xs-ls-c1
                        div.c2.xs-ls-c2
                        div.c3.xs-ls-c3
                        div.subscription 
                            h1 xs 
                            h5 -600
                            h6 handset
                    div.layout-element.layout-wrape-sm  
                        div.c1.sm-ls-c1
                        div.c2.sm-ls-c2
                        div.c3.sm-ls-c3
                        div.subscription 
                            h1 sm 
                            h5 600-960
                            h6 tablet
                    div.layout-element.layout-wrape-md 
                        div.c1.md-ls-c1
                        div.c2.md-ls-c2
                        div.c3.md-ls-c3
                        div.subscription 
                            h1 md 
                            h5 960-1264
                            h6 tablet
                            h6 laptop
                    div.layout-element.layout-wrape-lg 
                        div.d-flex 
                            div.c1.lg-ls-c1
                            div.right-element
                                div.c2.lg-ls-c2
                                div.c3.lg-ls-c3
                        div.subscription 
                            h1 lg 
                            h5 1264-1904 
                            h6 desktop
                    div.layout-element.layout-wrape-xl 
                        div.d-flex 
                            div.c1.xl-ls-c1
                            div.right-element
                                div.c2.lg-ls-c2
                                div.c3.lg-ls-c3
                        div.subscription 
                            h1 xl
                            h5 1904-
                            h6 4k
                            h6 ultra-wides
        v-col(cols="12" sm="12" md="12" lg="6")
            v-sheet(class="pa-12" color="grey lighten-3" )
                nuxt-link(to="respPattern/tinyTweaks")
                    h1.mb-4 Tiny tweaks 
                    h4 Tiny tweaks では、フォントサイズの調整、画像のリサイズ、コンテンツの移動など、レイアウトの微調整を行います。
                    h4 このパターンは、1 ページから成るリニアなウェブサイトや、テキストの多い記事サイトなど、一列で構成されるレイアウトに適しています。
                div.layout-grp
                    div.layout-element.layout-wrape-xs 
                        div.c1.xs-tt-c1
                        div.subscription 
                            h1 xs 
                            h5 -600
                            h6 handset
                    div.layout-element.layout-wrape-sm  
                        div.c1.sm-tt-c1
                        div.subscription 
                            h1 sm 
                            h5 600-960
                            h6 tablet
                    div.layout-element.layout-wrape-md 
                        div.c1.md-tt-c1
                        div.subscription 
                            h1 md 
                            h5 960-1264
                            h6 tablet
                            h6 laptop
                    div.layout-element.layout-wrape-lg 
                        div.c1.lg-tt-c1
                        div.subscription 
                            h1 lg 
                            h5 1264-1904 
                            h6 desktop
                    div.layout-element.layout-wrape-xl 
                        div.c1.xl-tt-c1
                        div.subscription 
                            h1 xl
                            h5 1904-
                            h6 4k
                            h6 ultra-wides
        v-col(cols="12" sm="12" md="12" lg="6")
            v-sheet(class="pa-12" color="grey lighten-3" )
                nuxt-link(to="respPattern/offCanvas")
                    h1.mb-4 Off canvas 
                    h4 Off canvas パターンでは、コンテンツを縦にスタックせずに、ナビゲーションやアプリメニューのような使用頻度の低いコンテンツをオフスクリーンに配置します。
                    h4 これらのコンテンツは画面サイズが十分に大きい場合にのみ表示され、小さい画面ではクリックしたときのみ表示されます。
                div.layout-grp
                    div.layout-element.offCanvas-mg-xs 
                        div.d-flex.element-wrape-xs
                            div.c1.xs-oc-c1
                            div.c2.xs-oc-c2
                            div.c3.xs-oc-c3
                        div.subscription 
                            h1 xs 
                            h5 -600
                            h6 handset
                    div.layout-element.offCanvas-mg-sm
                        div.d-flex.element-wrape-sm  
                            div.c1.sm-oc-c1
                            div.c2.sm-oc-c2
                            div.c3.sm-oc-c3
                        div.subscription 
                            h1 sm 
                            h5 600-960
                            h6 tablet
                    div.layout-element.offCanvas-mg-md 
                        div.d-flex.element-wrape-md 
                            div.c1.md-oc-c1
                            div.c2.md-oc-c2
                            div.c3.md-oc-c3
                        div.subscription 
                            h1 md 
                            h5 960-1264
                            h6 tablet
                            h6 laptop
                    div.layout-element.layout-wrape-lg 
                        div.d-flex 
                            div.c1.lg-oc-c1
                            div.c2.lg-oc-c2
                            div.c3.lg-oc-c3
                        div.subscription 
                            h1 lg 
                            h5 1264-1904 
                            h6 desktop
                    div.layout-element.layout-wrape-xl 
                        div.d-flex 
                            div.c1.xl-oc-c1
                            div.c2.xl-oc-c2
                            div.c3.xl-oc-c3
                        div.subscription 
                            h1 xl
                            h5 1904-
                            h6 4k
                            h6 ultra-wides
    v-row 
        v-col(cols="12")
            //- v-btn.text-h3.pa-4(href="https://csslayout.io/patterns/")  CSS LAYOUT パターン
            v-btn(@click="isOpenCSSLayout=!isOpenCSSLayout")
                span.text-h3.mr-4.d-inline-block  LAYOUT 
                span.text-h5.mr-4.pa-1.d-inline-block.blue.white--text  CSS LAYOUT 
                v-icon(v-show="!isOpenCSSLayout") fas fa-angle-down
                v-icon(v-show="isOpenCSSLayout") fas fa-angle-up
            
    v-row(v-show="isOpenCSSLayout") 
        v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                v-card(color="grey lighten-3").pa-6 
                    div(class="d-flex flex-no-wrap justify-space-between")
                        div.flex-grow-0.flex-shrink-0   
                            v-card-title.headline 
                                 nuxt-link(to="template/cl-layout/card-layout") Card Layout (Grig) 
                            v-card-subtitle
                                nuxt-link(to="template/cl-layout/card-layout")
                                    div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                        div.layout-wrape 
                                            div.header-footer.bottom-line v-app-bar  
                                            div.card-element
                                                component( :is="'cardLayout'" )
                                            div.header-footer.top-line v-footer  
                            v-card-actions
                            v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                        div.flex-grow-1.flex-shrink-1   
                            v-card-title.headline.font-weight-bold Component
                            v-card-subtitle 
                                h3 Components / Grids
                                v-chip-group(column) 
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col  
        v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                v-card(color="grey lighten-3").pa-6 
                    div(class="d-flex flex-no-wrap justify-space-between")
                        div.flex-grow-0.flex-shrink-0   
                            v-card-title.headline 
                                 nuxt-link(to="template/cl-layout/holyGrail-layout") Holy Grail 
                            v-card-subtitle
                                nuxt-link(to="template/cl-layout/holyGrail-layout")
                                    div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                        div.layout-wrape 
                                            div.header-footer.bottom-line v-app-bar  
                                            div.card-element
                                                component( :is="'holyGrailIcons'" )
                                            div.header-footer.top-line v-footer  
                            v-card-actions
                            v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                        div.flex-grow-1.flex-shrink-1   
                            v-card-title.headline.font-weight-bold Component
                            v-card-subtitle 
                                h3 Components / Grids
                                v-chip-group(column) 
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col  
        v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                v-card(color="grey lighten-3").pa-6 
                    div(class="d-flex flex-no-wrap justify-space-between")
                        div.flex-grow-0.flex-shrink-0   
                            v-card-title.headline 
                                 nuxt-link(to="template/cl-layout/sameHeightColumn-layout") Sane Height Columns
                            v-card-subtitle
                                nuxt-link(to="template/cl-layout/sameHeightColumn-layout")
                                    div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                        div.layout-wrape 
                                            div.header-footer.bottom-line v-app-bar  
                                            div.card-element
                                                component( :is="'sameHightColumns'" )
                                            div.header-footer.top-line v-footer  
                            v-card-actions
                            v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                        div.flex-grow-1.flex-shrink-1   
                            v-card-title.headline.font-weight-bold Component
                            v-card-subtitle 
                                h3 Components / Grids
                                v-chip-group(column) 
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col  
        v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                v-card(color="grey lighten-3").pa-6 
                    div(class="d-flex flex-no-wrap justify-space-between")
                        div.flex-grow-0.flex-shrink-0   
                            v-card-title.headline 
                                 nuxt-link(to="template/cl-layout/sidebar-layout") Side Bar 
                            v-card-subtitle
                                nuxt-link(to="template/cl-layout/sidebar-layout")
                                    div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                        div.layout-wrape 
                                            div.header-footer.bottom-line v-app-bar  
                                            div.card-element
                                                component( :is="'sidebarIcons'" )
                                            div.header-footer.top-line v-footer  
                            v-card-actions
                            v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                        div.flex-grow-1.flex-shrink-1   
                            v-card-title.headline.font-weight-bold Component
                            v-card-subtitle 
                                h3 Components / Grids
                                v-chip-group(column) 
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col  
        v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                v-card(color="grey lighten-3").pa-6 
                    div(class="d-flex flex-no-wrap justify-space-between")
                        div.flex-grow-0.flex-shrink-0   
                            v-card-title.headline 
                                 nuxt-link(to="template/cl-layout/simpleGrid-layout") Simple Grid
                            v-card-subtitle
                                nuxt-link(to="template/cl-layout/simpleGrid-layout")
                                    div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                        div.layout-wrape 
                                            div.header-footer.bottom-line v-app-bar  
                                            div.card-element
                                                component( :is="'simpleGridIcons'" )
                                            div.header-footer.top-line v-footer  
                            v-card-actions
                            v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                        div.flex-grow-1.flex-shrink-1   
                            v-card-title.headline.font-weight-bold Component
                            v-card-subtitle 
                                h3 Components / Grids
                                v-chip-group(column) 
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col  
        v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                v-card(color="grey lighten-3").pa-6 
                    div(class="d-flex flex-no-wrap justify-space-between")
                        div.flex-grow-0.flex-shrink-0   
                            v-card-title.headline 
                                 nuxt-link(to="template/cl-layout/splitScreen-layout") Sprit Screen
                            v-card-subtitle
                                nuxt-link(to="template/cl-layout/splitScreen-layout")
                                    div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                        div.layout-wrape 
                                            div.header-footer.bottom-line v-app-bar  
                                            div.card-element
                                                component( :is="'splitScreenIcons'" )
                                            div.header-footer.top-line v-footer  
                            v-card-actions
                            v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                        div.flex-grow-1.flex-shrink-1   
                            v-card-title.headline.font-weight-bold Component
                            v-card-subtitle 
                                h3 Components / Grids
                                v-chip-group(column) 
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col  
        v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                v-card(color="grey lighten-3").pa-6 
                    div(class="d-flex flex-no-wrap justify-space-between")
                        div.flex-grow-0.flex-shrink-0   
                            v-card-title.headline 
                                 nuxt-link(to="template/cl-layout/stickyFooter-layout") Sticky Footer
                            v-card-subtitle
                                nuxt-link(to="template/cl-layout/stickyFooter-layout")
                                    div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                        div.layout-wrape 
                                            div.header-footer.bottom-line v-app-bar  
                                            div.card-element
                                                component( :is="'stickyFooterIcons'" )
                                            div.header-footer.top-line v-footer  
                            v-card-actions
                            v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                        div.flex-grow-1.flex-shrink-1   
                            v-card-title.headline.font-weight-bold Component
                            v-card-subtitle 
                                h3 Components / Grids
                                v-chip-group(column) 
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col  
        v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                v-card(color="grey lighten-3").pa-6 
                    div(class="d-flex flex-no-wrap justify-space-between")
                        div.flex-grow-0.flex-shrink-0   
                            v-card-title.headline 
                                 nuxt-link(to="template/cl-layout/stickyHeader-layout") Sticky Header
                            v-card-subtitle
                                nuxt-link(to="template/cl-layout/stickyHeader-layout")
                                    div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                        div.layout-wrape 
                                            div.header-footer.bottom-line v-app-bar  
                                            div.card-element
                                                component( :is="'stickyHeaderIcons'" )
                                            div.header-footer.top-line v-footer  
                            v-card-actions
                            v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                        div.flex-grow-1.flex-shrink-1   
                            v-card-title.headline.font-weight-bold Component
                            v-card-subtitle 
                                h3 Components / Grids
                                v-chip-group(column) 
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col  
        v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                v-card(color="grey lighten-3").pa-6 
                    div(class="d-flex flex-no-wrap justify-space-between")
                        div.flex-grow-0.flex-shrink-0   
                            v-card-title.headline 
                                 nuxt-link(to="template/cl-layout/stickySections-layout") Sticky Sections
                            v-card-subtitle
                                nuxt-link(to="template/cl-layout/stickySections-layout")
                                    div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                        div.layout-wrape 
                                            div.header-footer.bottom-line v-app-bar  
                                            div.card-element
                                                component( :is="'stickySectionsIcons'" )
                                            div.header-footer.top-line v-footer  
                            v-card-actions
                            v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                        div.flex-grow-1.flex-shrink-1   
                            v-card-title.headline.font-weight-bold Component
                            v-card-subtitle 
                                h3 Components / Grids
                                v-chip-group(column) 
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                                    v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col  

    v-row 
        v-col(cols="12")
            //- v-btn.text-h3.pa-4(href="https://csslayout.io/patterns/")  CSS LAYOUT パターン
            v-btn(@click="isOpenCSSNavigation=!isOpenCSSNavigation")
                span.text-h3.mr-4.d-inline-block  NAVIGATION 
                span.text-h5.mr-4.pa-1.d-inline-block.blue.white--text  CSS LAYOUT 
                v-icon(v-show="!isOpenCSSNavigation") fas fa-angle-down
                v-icon(v-show="isOpenCSSNavigation") fas fa-angle-up
                
        v-row(v-show="isOpenCSSNavigation") 
            v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                    v-card(color="grey lighten-3").pa-6 
                        div(class="d-flex flex-no-wrap justify-space-between")
                            div.flex-grow-0.flex-shrink-0   
                                v-card-title.headline 
                                    nuxt-link(to="template/cl-layout/breadcrumb-layout") Breadcrumb
                                v-card-subtitle
                                    nuxt-link(to="template/cl-layout/breadcrumb-layout")
                                        div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                            div.layout-wrape 
                                                div.header-footer.bottom-line v-app-bar  
                                                div.card-element
                                                    component( :is="'breadcrumbIcons'" )
                                                div.header-footer.top-line v-footer  
                                v-card-actions
                                v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                            div.flex-grow-1.flex-shrink-1   
                                v-card-title.headline.font-weight-bold Component
                                v-card-subtitle 
                                    h3 Components / Breadcrumbs
                                    v-chip-group(column) 
                                        v-chip(href="https://vuetifyjs.com/ja/components/breadcrumbs/") v-breadcrumbs
            v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                    v-card(color="grey lighten-1").pa-6 
                        div(class="d-flex flex-no-wrap justify-space-between")
                            div.flex-grow-0.flex-shrink-0   
                                v-card-title.headline 
                                    nuxt-link(to="template/cl-layout/card-layout") Circular Navigation
                                v-card-subtitle
                                    nuxt-link(to="template/cl-layout/card-layout")
                                        div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                            div.layout-wrape 
                                                div.header-footer.bottom-line v-app-bar  
                                                div.card-element
                                                    component( :is="'circularNavigationIcons'" )
                                                div.header-footer.top-line v-footer  
                                v-card-actions
                                v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                            div.flex-grow-1.flex-shrink-1   
                                v-card-title.headline.font-weight-bold Component
                                v-card-subtitle 
                                    h3 Components / Grids
                                    v-chip-group(column) 
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col                        
            v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                    v-card(color="grey lighten-1").pa-6 
                        div(class="d-flex flex-no-wrap justify-space-between")
                            div.flex-grow-0.flex-shrink-0   
                                v-card-title.headline 
                                    nuxt-link(to="template/cl-layout/card-layout") Dot Navigation
                                v-card-subtitle
                                    nuxt-link(to="template/cl-layout/card-layout")
                                        div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                            div.layout-wrape 
                                                div.header-footer.bottom-line v-app-bar  
                                                div.card-element
                                                    component( :is="'dotNavigationIcons'" )
                                                div.header-footer.top-line v-footer  
                                v-card-actions
                                v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                            div.flex-grow-1.flex-shrink-1   
                                v-card-title.headline.font-weight-bold Component
                                v-card-subtitle 
                                    h3 Components / Grids
                                    v-chip-group(column) 
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col                        
            v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                    v-card(color="grey lighten-1").pa-6 
                        div(class="d-flex flex-no-wrap justify-space-between")
                            div.flex-grow-0.flex-shrink-0   
                                v-card-title.headline 
                                    nuxt-link(to="template/cl-layout/card-layout") Drawer
                                v-card-subtitle
                                    nuxt-link(to="template/cl-layout/card-layout")
                                        div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                            div.layout-wrape 
                                                div.header-footer.bottom-line v-app-bar  
                                                div.card-element
                                                    component( :is="'drawerIcons'" )
                                                div.header-footer.top-line v-footer  
                                v-card-actions
                                v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                            div.flex-grow-1.flex-shrink-1   
                                v-card-title.headline.font-weight-bold Component
                                v-card-subtitle 
                                    h3 Components / Grids
                                    v-chip-group(column) 
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col                        
            v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                    v-card(color="grey lighten-3").pa-6 
                        div(class="d-flex flex-no-wrap justify-space-between")
                            div.flex-grow-0.flex-shrink-0   
                                v-card-title.headline 
                                    nuxt-link(to="template/cl-layout/dropdown-layout") Dropdown(Menus)
                                v-card-subtitle
                                    nuxt-link(to="template/cl-layout/dropdown-layout")
                                        div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                            div.layout-wrape 
                                                div.header-footer.bottom-line v-app-bar  
                                                div.card-element
                                                    component( :is="'dropdownIcons'" )
                                                div.header-footer.top-line v-footer  
                                v-card-actions
                                v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                            div.flex-grow-1.flex-shrink-1   
                                v-card-title.headline.font-weight-bold Component
                                v-card-subtitle 
                                    h3 Components / Menus
                                    v-chip-group(column) 
                                        v-chip(href="https://vuetifyjs.com/ja/components/menus/") v-menu
            v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                    v-card(color="grey lighten-1").pa-6 
                        div(class="d-flex flex-no-wrap justify-space-between")
                            div.flex-grow-0.flex-shrink-0   
                                v-card-title.headline 
                                    nuxt-link(to="template/cl-layout/card-layout") Full Screen Menu
                                v-card-subtitle
                                    nuxt-link(to="template/cl-layout/card-layout")
                                        div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                            div.layout-wrape 
                                                div.header-footer.bottom-line v-app-bar  
                                                div.card-element
                                                    component( :is="'fullScreenMenuIcons'" )
                                                div.header-footer.top-line v-footer  
                                v-card-actions
                                v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                            div.flex-grow-1.flex-shrink-1   
                                v-card-title.headline.font-weight-bold Component
                                v-card-subtitle 
                                    h3 Components / Grids
                                    v-chip-group(column) 
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col                        
            v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                    v-card(color="grey lighten-1").pa-6 
                        div(class="d-flex flex-no-wrap justify-space-between")
                            div.flex-grow-0.flex-shrink-0   
                                v-card-title.headline 
                                    nuxt-link(to="template/cl-layout/card-layout") Mega Menu
                                v-card-subtitle
                                    nuxt-link(to="template/cl-layout/card-layout")
                                        div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                            div.layout-wrape 
                                                div.header-footer.bottom-line v-app-bar  
                                                div.card-element
                                                    component( :is="'megaMenuIcons'" )
                                                div.header-footer.top-line v-footer  
                                v-card-actions
                                v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                            div.flex-grow-1.flex-shrink-1   
                                v-card-title.headline.font-weight-bold Component
                                v-card-subtitle 
                                    h3 Components / Grids
                                    v-chip-group(column) 
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col                        
            v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                    v-card(color="grey lighten-3").pa-6 
                        div(class="d-flex flex-no-wrap justify-space-between")
                            div.flex-grow-0.flex-shrink-0   
                                v-card-title.headline 
                                    nuxt-link(to="template/cl-layout/menu-layout") Menu(List Item Groups)
                                v-card-subtitle
                                    nuxt-link(to="template/cl-layout/menu-layout")
                                        div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                            div.layout-wrape 
                                                div.header-footer.bottom-line v-app-bar  
                                                div.card-element
                                                    component( :is="'menuIcons'" )
                                                div.header-footer.top-line v-footer  
                                v-card-actions
                                v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                            div.flex-grow-1.flex-shrink-1   
                                v-card-title.headline.font-weight-bold Component
                                v-card-subtitle 
                                    //- h3 Components / Lists
                                    //- v-chip-group(column) 
                                    //-     v-chip(href="https://vuetifyjs.com/ja/components/lists/") v-list 
                                    //-     v-chip(href="https://vuetifyjs.com/ja/components/lists/") v-list-item 
                                    //-     v-chip(href="https://vuetifyjs.com/ja/components/lists/") v-list-group
                                        //- v-chip(href="https://vuetifyjs.com/ja/components/lists/") v-list-item-action
                                        //- v-chip(href="https://vuetifyjs.com/ja/components/lists/") v-list-item-avater
                                        //- v-chip(href="https://vuetifyjs.com/ja/components/lists/") v-list-item-content
                                    h3 Components / List Item Groups
                                    v-chip-group(column) 
                                        v-chip(href="https://vuetifyjs.com/ja/components%20/list-item-groups/") v-list-item-group 
                                        v-chip(href="https://vuetifyjs.com/ja/components%20/list-item-groups/") v-list-item  
                                        //- v-chip(href="https://vuetifyjs.com/ja/components%20/list-item-groups/") v-list-item-action                        
                                        //- v-chip(href="https://vuetifyjs.com/ja/components%20/list-item-groups/") v-list-item-avater                        
                                        //- v-chip(href="https://vuetifyjs.com/ja/components%20/list-item-groups/") v-list-item-content                        
                                        //- v-chip(href="https://vuetifyjs.com/ja/components%20/list-item-groups/") v-list-item-subtitle                        
                                        //- v-chip(href="https://vuetifyjs.com/ja/components%20/list-item-groups/") v-list-item-action-text                      
            v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                    v-card(color="grey lighten-1").pa-6 
                        div(class="d-flex flex-no-wrap justify-space-between")
                            div.flex-grow-0.flex-shrink-0   
                                v-card-title.headline 
                                    nuxt-link(to="template/cl-layout/card-layout") Nested Dropdown
                                v-card-subtitle
                                    nuxt-link(to="template/cl-layout/card-layout")
                                        div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                            div.layout-wrape 
                                                div.header-footer.bottom-line v-app-bar  
                                                div.card-element
                                                    component( :is="'nestedDropdownsIcons'" )
                                                div.header-footer.top-line v-footer  
                                v-card-actions
                                v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                            div.flex-grow-1.flex-shrink-1   
                                v-card-title.headline.font-weight-bold Component
                                v-card-subtitle 
                                    h3 Components / Grids
                                    v-chip-group(column) 
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col                        
            v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                    v-card(color="grey lighten-3").pa-6 
                        div(class="d-flex flex-no-wrap justify-space-between")
                            div.flex-grow-0.flex-shrink-0   
                                v-card-title.headline 
                                    nuxt-link(to="template/cl-layout/pagination-layout") pagination
                                v-card-subtitle
                                    nuxt-link(to="template/cl-layout/pagination-layout")
                                        div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                            div.layout-wrape 
                                                div.header-footer.bottom-line v-app-bar  
                                                div.card-element
                                                    component( :is="'paginationIcons'" )
                                                div.header-footer.top-line v-footer  
                                v-card-actions
                                v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                            div.flex-grow-1.flex-shrink-1   
                                v-card-title.headline.font-weight-bold Component
                                v-card-subtitle 
                                    h3 Components / Paginations
                                    v-chip-group(column) 
                                        v-chip(href="https://vuetifyjs.com/ja/components/paginations/") v-pagination 
            v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                    v-card(color="grey lighten-1").pa-6 
                        div(class="d-flex flex-no-wrap justify-space-between")
                            div.flex-grow-0.flex-shrink-0   
                                v-card-title.headline 
                                    nuxt-link(to="template/cl-layout/card-layout") Previus Next Button
                                v-card-subtitle
                                    nuxt-link(to="template/cl-layout/card-layout")
                                        div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                            div.layout-wrape 
                                                div.header-footer.bottom-line v-app-bar  
                                                div.card-element
                                                    component( :is="'PreviousAndNextButtonsIcons'" )
                                                div.header-footer.top-line v-footer  
                                v-card-actions
                                v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                            div.flex-grow-1.flex-shrink-1   
                                v-card-title.headline.font-weight-bold Component
                                v-card-subtitle 
                                    h3 Components / Grids
                                    v-chip-group(column) 
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col                        
            v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                    v-card(color="grey lighten-1").pa-6 
                        div(class="d-flex flex-no-wrap justify-space-between")
                            div.flex-grow-0.flex-shrink-0   
                                v-card-title.headline 
                                    nuxt-link(to="template/cl-layout/card-layout") Split Navigation
                                v-card-subtitle
                                    nuxt-link(to="template/cl-layout/card-layout")
                                        div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                            div.layout-wrape 
                                                div.header-footer.bottom-line v-app-bar  
                                                div.card-element
                                                    component( :is="'splitNavigationIcons'" )
                                                div.header-footer.top-line v-footer  
                                v-card-actions
                                v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                            div.flex-grow-1.flex-shrink-1   
                                v-card-title.headline.font-weight-bold Component
                                v-card-subtitle 
                                    h3 Components / Grids
                                    v-chip-group(column) 
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col                        
            v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                    v-card(color="grey lighten-3").pa-6 
                        div(class="d-flex flex-no-wrap justify-space-between")
                            div.flex-grow-0.flex-shrink-0   
                                v-card-title.headline 
                                    nuxt-link(to="template/cl-layout/tab-layout") Tab
                                v-card-subtitle
                                    nuxt-link(to="template/cl-layout/tab-layout")
                                        div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                            div.layout-wrape 
                                                div.header-footer.bottom-line v-app-bar  
                                                div.card-element
                                                    component( :is="'tabIcons'" )
                                                div.header-footer.top-line v-footer  
                                v-card-actions
                                v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                            div.flex-grow-1.flex-shrink-1   
                                v-card-title.headline.font-weight-bold Component
                                v-card-subtitle 
                                    h3 Components / Tabs
                                    v-chip-group(column) 
                                        v-chip(href="https://vuetifyjs.com/ja/components/tabs/") v-tabs 
                                        v-chip(href="https://vuetifyjs.com/ja/components/tabs/") v-tab  
                                        v-chip(href="https://vuetifyjs.com/ja/components/tabs/") v-tabs-items                         
                                        v-chip(href="https://vuetifyjs.com/ja/components/tabs/") v-tab-items                         
                                        //- v-chip(href="https://vuetifyjs.com/ja/components/tabs/") v-tabs-slider                     
            v-col(cols="12" sm="12" md="12" lg="6" xl="4")
                    v-card(color="grey lighten-1").pa-6 
                        div(class="d-flex flex-no-wrap justify-space-between")
                            div.flex-grow-0.flex-shrink-0   
                                v-card-title.headline 
                                    nuxt-link(to="template/cl-layout/card-layout") Wizard
                                v-card-subtitle
                                    nuxt-link(to="template/cl-layout/card-layout")
                                        div.d-flex.align-start.justify-start.flex-grow-0.flex-shrink-0 
                                            div.layout-wrape 
                                                div.header-footer.bottom-line v-app-bar  
                                                div.card-element
                                                    component( :is="'wizardIcons'" )
                                                div.header-footer.top-line v-footer  
                                v-card-actions
                                v-btn(text href="https://vuetifyjs.com/ja/components/application/") Vuetify  Components/Application
                            div.flex-grow-1.flex-shrink-1   
                                v-card-title.headline.font-weight-bold Component
                                v-card-subtitle 
                                    h3 Components / Grids
                                    v-chip-group(column) 
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-container 
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-row  
                                        v-chip(href="https://vuetifyjs.com/ja/components/grids/") v-col                        
                                


</template>
<script>
import headerFooter from '~/components/iconsCssLayout/headerFooter.vue'
import cardLayout from '~/components/iconsCssLayout/cardLayout.vue'
import sameHightColumns from '~/components/iconsCssLayout/sameHightColumns.vue'
import holyGrailIcons from '~/components/iconsCssLayout/holyGrailIcons.vue'
import sidebarIcons from '~/components/iconsCssLayout/sidebarIcons.vue'
import simpleGridIcons from '~/components/iconsCssLayout/simpleGridIcons.vue'
import splitScreenIcons from '~/components/iconsCssLayout/splitScreenIcons.vue'
import stickyFooterIcons from '~/components/iconsCssLayout/stickyFooterIcons.vue'
import stickyHeaderIcons from '~/components/iconsCssLayout/stickyHeaderIcons.vue'
import stickySectionsIcons from '~/components/iconsCssLayout/stickySectionsIcons.vue'
import breadcrumbIcons from '~/components/iconsCssLayout/breadcrumbIcons.vue'
import circularNavigationIcons from '~/components/iconsCssLayout/circularNavigationIcons.vue'
import dotNavigationIcons from '~/components/iconsCssLayout/dotNavigationIcons.vue'
import drawerIcons from '~/components/iconsCssLayout/drawerIcons.vue'
import dropdownIcons from '~/components/iconsCssLayout/dropdownIcons.vue'
import fullScreenMenuIcons from '~/components/iconsCssLayout/fullScreenMenuIcons.vue'
import megaMenuIcons from '~/components/iconsCssLayout/megaMenuIcons.vue'
import menuIcons from '~/components/iconsCssLayout/menuIcons.vue'
import nestedDropdownsIcons from '~/components/iconsCssLayout/nestedDropdownsIcons.vue'
import paginationIcons from '~/components/iconsCssLayout/paginationIcons.vue'
import PreviousAndNextButtonsIcons from '~/components/iconsCssLayout/PreviousAndNextButtonsIcons.vue'
import splitNavigationIcons from '~/components/iconsCssLayout/splitNavigationIcons.vue'
import tabIcons from '~/components/iconsCssLayout/tabIcons.vue'
import WizardIcons from '~/components/iconsCssLayout/WizardIcons.vue'

export default {
  layout: 'sidebarNav-vuetify',
  components: {
    headerFooter,
    cardLayout,
    sameHightColumns,
    holyGrailIcons,
    sidebarIcons,
    simpleGridIcons,
    splitScreenIcons,
    stickyFooterIcons,
    stickyHeaderIcons,
    stickySectionsIcons,
    breadcrumbIcons,
    circularNavigationIcons,
    dotNavigationIcons,
    drawerIcons,
    dropdownIcons,
    fullScreenMenuIcons,
    megaMenuIcons,
    menuIcons,
    nestedDropdownsIcons,
    paginationIcons,
    PreviousAndNextButtonsIcons,
    splitNavigationIcons,
    tabIcons,
    WizardIcons,
  },
  data() {
    return {
      isOpenResponsivePattern: false,
      isOpenCSSLayout: false,
      isOpenCSSNavigation: false,
    }
  },
}
</script>
<style scoped lang="scss">
.layout-wrape {
  border: 1px solid rgba(0, 0, 0, 0.3);
  border-radius: 2px;
  box-shadow: rgba(0, 0, 0, 0.2) 0px 16px 24px -4px,
    rgba(0, 0, 0, 0.05) 0px 8px 8px -4px;
  height: 192px;
  width: 160px;
  overflow: hidden;
  position: relative;
}
.header-footer {
  width: 100%;
  height: 16px;
  text-align: center;
}
.top-line {
  border-top: 1px solid rgba(0, 0, 0, 0.3);
}
.bottom-line {
  border-bottom: 1px solid rgba(0, 0, 0, 0.3);
}
.card-element {
  height: 160px;
  width: 160px;
  overflow: hidden;
  position: relative;
}
.layout-grp {
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-start;
  align-items: center;
  margin-top: 16px;
  border: 1px solid grey;
  padding: 16px;
}
.layout-element {
  border: 2px solid rgba(0, 0, 0, 1);
  border-radius: 4px;
  box-shadow: rgba(0, 0, 0, 0.2) 0px 16px 24px -4px,
    rgba(0, 0, 0, 0.05) 0px 8px 8px -4px;
  height: 120px;
  width: 60px;
  position: relative;
  margin: 16px 16px 150px 16px;
  position: relative;
}

.subscription {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: white;
}
.layout-wrape-xs {
  width: 60px;
}
.layout-wrape-sm {
  width: 90px;
}
.layout-wrape-md {
  width: 120px;
}
.layout-wrape-lg {
  width: 190px;
  padding-right: 20px;
  padding-left: 20px;
}
.layout-wrape-xl {
  width: 240px;
  padding-right: 40px;
  padding-left: 40px;
}
.offCanvas-mg-xs {
  width: 60px;
  height: 120px;
  margin-right: 70px;
  margin-left: 70px;
}
.offCanvas-mg-sm {
  width: 90px;
  height: 120px;
  margin-right: 70px;
  margin-left: 70px;
}
.offCanvas-mg-md {
  width: 120px;
  height: 120px;
  margin-right: 70px;
  margin-left: 70px;
}
.element-wrape-xs {
  position: absolute;
  top: 0;
  left: -60px;
  width: 180px;
  height: 120px;
}
.element-wrape-sm {
  position: absolute;
  top: 0;
  left: -45px;
  width: 135px;
  height: 120px;
}
.element-wrape-md {
  position: absolute;
  top: 0;
  left: -60px;
  width: 180px;
  height: 120px;
}
.c1 {
  background-color: rgba(4, 33, 161, 0.5);
}
.c2 {
  background-color: rgba(3, 151, 250, 0.5);
}
.c3 {
  background-color: rgba(2, 109, 20, 0.5);
}
.c4 {
  background-color: rgba(163, 134, 4, 0.5);
}
.c5 {
  background-color: rgba(141, 5, 11, 0.5);
}
//mostly
.xs-c1 {
  width: 100%;
  height: 140px;
}
.xs-c2 {
  width: 100%;
  height: 30px;
}
.xs-c3 {
  width: 100%;
  height: 30px;
}
.xs-c4 {
  width: 100%;
  height: 30px;
}
.xs-c5 {
  width: 100%;
  height: 30px;
}
.sm-c1 {
  width: 100%;
  height: 70px;
}
.sm-c2 {
  width: 50%;
  height: 50px;
}
.sm-c3 {
  width: 50%;
  height: 50px;
}
.sm-c4 {
  width: 50%;
  height: 30px;
}
.sm-c5 {
  width: 50%;
  height: 30px;
}
.md-c1 {
  width: 100%;
  height: 60px;
}
.md-c2 {
  width: 50%;
  height: 40px;
}
.md-c3 {
  width: 50%;
  height: 40px;
}
.md-c4 {
  width: 50%;
  height: 20px;
}
.md-c5 {
  width: 50%;
  height: 20px;
}
.lg-c1 {
  width: 60%;
  height: 60px;
}
.lg-c2 {
  width: 40%;
  height: 60px;
}
.lg-c3 {
  width: 33.3333%;
  height: 60px;
}
.lg-c4 {
  width: 33.333%;
  height: 60px;
}
.lg-c5 {
  width: 33.333%;
  height: 60px;
}
.xl-c1 {
  width: 60%;
  height: 60px;
}
.xl-c2 {
  width: 40%;
  height: 60px;
}
.xl-c3 {
  width: 33.3333%;
  height: 60px;
}
.xl-c4 {
  width: 33.333%;
  height: 60px;
}
.xl-c5 {
  width: 33.333%;
  height: 60px;
}
//colum drop
.xs-cd-c1 {
  width: 100%;
  height: 140px;
}
.xs-cd-c2 {
  width: 100%;
  height: 30px;
}
.xs-cd-c3 {
  width: 100%;
  height: 30px;
}

.sm-cd-c1 {
  width: 100%;
  height: 70px;
}
.sm-cd-c2 {
  width: 100%;
  height: 50px;
}
.sm-cd-c3 {
  width: 100%;
  height: 50px;
}

.md-cd-c1 {
  width: 40%;
  height: 120px;
}
.md-cd-c2 {
  width: 60%;
  height: 120px;
}
.md-cd-c3 {
  width: 100%;
  height: 40px;
}

.lg-cd-c1 {
  width: 30%;
  height: 120px;
}
.lg-cd-c2 {
  width: 40%;
  height: 120px;
}
.lg-cd-c3 {
  width: 30%;
  height: 120px;
}

.xl-cd-c1 {
  width: 20%;
  height: 120px;
}
.xl-cd-c2 {
  width: 60%;
  height: 120px;
}
.xl-cd-c3 {
  width: 20%;
  height: 120px;
}
//Layout shifter
.xs-ls-c1 {
  width: 100%;
  height: 30px;
}
.xs-ls-c2 {
  width: 100%;
  height: 90px;
}
.xs-ls-c3 {
  width: 100%;
  height: 90px;
}

.sm-ls-c1 {
  width: 100%;
  height: 20px;
}
.sm-ls-c2 {
  width: 100%;
  height: 60px;
}
.sm-ls-c3 {
  width: 100%;
  height: 60px;
}

.md-ls-c1 {
  width: 100%;
  height: 15px;
}
.md-ls-c2 {
  width: 100%;
  height: 55px;
}
.md-ls-c3 {
  width: 100%;
  height: 50px;
}

.lg-ls-c1 {
  width: 30px;
  height: 120px;
}
.lg-ls-c2 {
  width: 100%;
  height: 60px;
}
.lg-ls-c3 {
  width: 100%;
  height: 60px;
}

.xl-ls-c1 {
  width: 30px;
  height: 120px;
}
.xl-ls-c2 {
  width: 100%;
  height: 60px;
}
.xl-ls-c3 {
  width: 100%;
  height: 60px;
}
.right-element {
  width: 100%;
  height: 120px;
}
//tiny tweaks
.xs-tt-c1 {
  width: 100%;
  height: 120px;
}
.sm-tt-c1 {
  width: 100%;
  height: 120px;
}
.md-tt-c1 {
  width: 100%;
  height: 120px;
}
.lg-tt-c1 {
  width: 100%x;
  height: 120px;
}
.xl-tt-c1 {
  width: 100%;
  height: 120px;
}
//Off Canvas
.xs-oc-c1 {
  width: 100%;
  height: 120px;
  //   flex: 60px;
}
.xs-oc-c2 {
  width: 100%;
  height: 120px;
  //   flex: 60px;
}
.xs-oc-c3 {
  width: 100%;
  height: 120px;
  //   flex: 60px;
}

.sm-oc-c1 {
  width: 100%;
  height: 120px;
}
.sm-oc-c2 {
  width: 100%;
  height: 120px;
}
.sm-oc-c3 {
  width: 100%;
  height: 120px;
}

.md-oc-c1 {
  width: 100%;
  height: 120px;
}
.md-oc-c2 {
  width: 100%;
  height: 120px;
}
.md-oc-c3 {
  width: 100%;
  height: 120px;
}

.lg-oc-c1 {
  width: 100px;
  height: 120px;
}
.lg-oc-c2 {
  width: 100%;
  height: 120px;
}
.lg-oc-c3 {
  width: 100%;
  height: 120px;
}

.xl-oc-c1 {
  width: 100px;
  height: 120px;
}
.xl-oc-c2 {
  width: 100%;
  height: 120px;
}
.xl-oc-c3 {
  width: 100%;
  height: 120px;
}
</style>
