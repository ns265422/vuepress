# VuePress 驅動的靜態站點生成工具

文件中有說明跟幾個市面上常見的靜態頁面產生做比較，包含 Nuxt（這我不太理解，因為這個是屬於應用，怎麼會跟他做比較）作者也說 VuePress 是專注於內容為中心的靜態頁面，並且當成文件使用，而不是應用。Docsify/Docute 是一個應用的文件產生器，但他沒有 SEO，如果只是單純的內部文件妥妥的。Hexo 是 Vue.js 官方網站一直在用的產生器，但它的佈景主題是真靜態，而且都是靠設定檔，但作者想要用更多的 vue.js 做一些交互跟 layout，還有最重要的是 markdown 渲染不靈活，是固定的。

---
# 什麼是VuePress

VuePress由兩部分組成：一個基於Vue的輕量級靜態網站生成器，以及為編寫技術文檔而優化的默認主題。 它是為了滿足Vue自己的子項目文檔的需求而創建的。
VuePress為每一個由它生成的頁面提供預加載的html，不僅加載速度極佳，同時對seo非常友好。一旦頁面被加載之後，Vue就全面接管所有的靜態內容，使其變成一個完全的SPA應用，其他的頁面也會在用戶使用導航進入的時候來按需加載。

---
#VuePress是怎樣運作的

一個VuePress應用實際上就是基於Vue、VueRouter以及webpack,如果你以前就用過vue,那麼當你在用VuePress開發或者定製自己的主題的時候，你會發現使用體驗幾乎是一毛一樣~你甚至可以用Vue DevTools來debug你的定製主題！
在build的過程中，VuePress會通過創建一個服務端渲染的版本，並訪問每一個路由來渲染相關的html。這種方法是來自Nuxt的nuxt generate命令,和其他項目如Gatsby的啟發。
每個markdown文件都被編譯為HTML，然後作為Vue組件的模板進行處理。這樣你可以在markdown文件中直接使用Vue，這在需要嵌入動態內容的時候非常有用。

---
#VuePress特性
1. 內置的markdown擴展專為技術文檔優化
2. 可以在markdown文件中直接使用vue
3. vue驅動的可定製畫主題
4. 支持PWA - Progressive Web App（漸進式網頁應用程序）
5. 集成Google Analytics
6. 響應式佈局
7. 可選的主頁
8. 一個簡單的頭部搜索組件
9. 可定製的導航欄和側邊欄
10. 自動生成的GitHub鏈接和頁面編輯鏈接

- [VuePress 中文網](https://www.vuepress.cn/)
- [VuePress手把手一小時快速踩坑- 掘金](https://juejin.im/post/5ad69f6c51882579ef4f7b12)
- [VuePress 快速踩坑](https://zhuanlan.zhihu.com/p/36116211)
- [VuePress - 基於Vue的靜態網站生成器](https://segmentfault.com/a/1190000014388622)