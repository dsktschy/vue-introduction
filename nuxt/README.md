# Nuxt  
Nuxt.jsを導入し、ポートフォリオサイトを開発します。  
[完成形](https://vue-introduction-nuxt.netlify.com)

## 構成
* [Step-1](./step-1)  
    * Nuxt.jsの導入。  
      Nuxt.jsの雛形を構築します。  
    * [[`vue init nuxt-community/starter-template app-name` の実行結果](https://github.com/dsktschy/vue-introduction/commit/18dfe5a#diff-de392a4?diff=split)]  
* [Step-2](./step-2)  
    * layoutsディレクトリとpagesディレクトリ。  
      ポートフォリオサイトを構成する4つのページを作成し、ページ間で共用されるパーツを作成します。  
    * [[Step-1からの変更点](https://github.com/dsktschy/vue-introduction/commit/d1b9e09#diff-de392a4?diff=split)]  
* [Step-3](./step-3)  
    * nuxt-linkコンポーネントについて。  
      ページ間共用のパーツに各ページをつなぐナビゲーションを設置します。  
    * [[Step-2からの変更点](https://github.com/dsktschy/vue-introduction/commit/69bbc97#diff-de392a4?diff=split)]  
* [Step-4](./step-4)  
    * 設定ファイルについて。  
      ページ間共用のスタイルと、headタグ内の情報を設定します。  
    * [[Step-3からの変更点](https://github.com/dsktschy/vue-introduction/commit/181408b0#diff-de392a4?diff=split)]  
* [Step-5](./step-5)  
    * $routeプロパティについて。  
      ページに応じてHTMLのクラスを変更し、見た目に変化をつけます。  
    * [[Step-4からの変更点](https://github.com/dsktschy/vue-introduction/commit/29b4590#diff-de392a4?diff=split)]  
* [Step-6](./step-6)  
    * 各ページにコンテンツを用意します。  
    * [[Step-5からの変更点](https://github.com/dsktschy/vue-introduction/commit/b3e7369#diff-de392a4?diff=split)]  
* [Step-7](./step-7)  
    * [CLI/Step-7](../cli/step-7)のモーダルウインドウを移植します。  
    * [[Step-6からの変更点](https://github.com/dsktschy/vue-introduction/commit/0e7b7f5#diff-de392a4?diff=split)]  

## Nuxt.jsとは
* Vue.jsの様々な周辺機能を1つにまとめたフレームワーク
* 最大の特徴は、Vue.jsアプリケーションを静的に生成する機能
  * SSR（サーバーサイドレンダリング）
  * 静的サイトの生成

### メリット
* 周辺機能の設定作業をスキップできる
* WebサイトからWebアプリケーションまで幅広く制作が可能
* 最近のフロントエンド開発技術の実行環境がほとんど揃う
* 表示差分とURLのみの書き換えにより、高速なページ遷移を実現可能

参考:  
https://ja.nuxtjs.org/
