# CLI  
Vue CLIを導入し、モーダルウインドウのコンポーネントを開発します。  
[完成形](https://vue-introduction-cli.netlify.com)

## 構成
* [Step-1](./step-1)  
    * Vue CLIの導入。  
      Vue.jsアプリケーションの雛形を構築します。  
    * [[`vue create app-name` の実行結果](https://github.com/dsktschy/vue-introduction/commit/d78cf8d#diff-7d36e1b?diff=split)]  
* [Step-2](./step-2)  
    * 単一ファイルコンポーネント（.vueファイル）の書式について。  
      [Basic/Step-3](../basic/step-3)で作成したコンポーネントを移植します。  
    * [[Step-1からの変更点](https://github.com/dsktschy/vue-introduction/commit/64563f7#diff-7d36e1b?diff=split)]  
* [Step-3](./step-3)  
    * Scoped CSSについて。  
      モーダルウインドウを表現するAppModalコンポーネントを作成します。  
    * [[Step-2からの変更点](https://github.com/dsktschy/vue-introduction/commit/f7cf29d#diff-7d36e1b?diff=split)]  
* [Step-4](./step-4)  
    * ディレクティブとプロパティとバインディング。  
      モーダルウインドウの開閉状態を管理します。  
    * [[Step-3からの変更点](https://github.com/dsktschy/vue-introduction/commit/589fed4#diff-7d36e1b?diff=split)]  
* [Step-5](./step-5)  
    * イベントとメソッド。  
      モーダルウインドウをクリックによって開閉可能にします。  
    * [[Step-4からの変更点](https://github.com/dsktschy/vue-introduction/commit/bc564cc#diff-7d36e1b?diff=split)]  
* [Step-6](./step-6)  
    * 要素の反復とスタイルのバインディング。  
      押下されたボタンに応じて、モーダルウインドウに異なる内容を表示します。  
    * [[Step-5からの変更点](https://github.com/dsktschy/vue-introduction/commit/e418c1b#diff-7d36e1b?diff=split)]  
* [Step-7](./step-7)  
    * トランジション効果について。  
      モーダルウインドウの開閉にフェードイン／アウト効果をつけます。  
    * [[Step-6からの変更点](https://github.com/dsktschy/vue-introduction/commit/50e4f67#diff-7d36e1b?diff=split)]  

## Vue CLIとは
* Vue.jsを使用するアプリケーションを簡単に構築するツール
* ターミナル上でコマンドによって操作する

### メリット
* Webpackの詳解と設定作業をスキップできる
* 様々な形式のアプリケーションを構築可能
  * 後述のフレームワークNuxt.jsもVue CLIを用いて構築できます。

参考:  
https://cli.vuejs.org/
