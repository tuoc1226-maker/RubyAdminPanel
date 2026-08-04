# RubyAdminPanel

[🇯🇵 日本語](README.md) | [🇺🇸 English](README.en.md)

Railsで柔軟かつ強力な管理ダッシュボードを作成するためのフレームワーク。

![RubyAdminPanel](https://user-images.githubusercontent.com/11917/72203824-ec10f980-3468-11ea-9ac1-51cd28ff88b7.png)

## RubyAdminPanelとは？

RubyAdminPanelは、管理ダッシュボードを生成するRailsライブラリです。これにより、
ユーザーはアプリケーション内のあらゆるモデルのレコードを作成、編集、検索、削除できる、洗練されたインターフェースを利用できます。
RubyAdminPanelは、最高のユーザーエクスペリエンスを提供し、可能な限り多くの作業を自動化すると同時に、
カスタマイズの柔軟性も備えています。

これらの目標を達成するために、RubyAdminPanelは以下のいくつかの基本原則に従っています。

* 標準のRailsにできる限り忠実であり、

RubyAdminPanel固有のコードは可能な限り最小限に抑えます。
* 最もシンプルなユースケースをサポートし、

ユーザーが標準のRailsコントローラーやビューなどのツールを使ってデフォルト設定を上書きできるようにします。
* ライブラリをコアコンポーネントとプラグインに分割し、

各コンポーネントが小さく、保守しやすい状態を維持します。

## 使用方法

RubyAdminPanelは[Rails Engine][]ですが、
新しい変更の貢献やテストに必要なすべてのものが同梱されています。

複数の依存関係バージョンとの互換性を維持するために、
[Appraisal][]を使用しています。

[Rails Engine]: https://guides.rubyonrails.org/engines.html

### はじめに

1. リポジトリをフォークします。
2. `./bin/setup` を実行して、基本依存関係をインストールし、ローカルデータベースをセットアップします。

3. テストスイートを実行します: `bundle exec rspec && bundle exec appraisal rspec`
4. 変更を加えます。
5. フォークしたリポジトリをプッシュし、プルリクエストを作成します。

優れたプルリクエストは、可能な限り小さな問題を解決し、十分なテストカバレッジを持ち、（必要に応じて）国際化に対応している必要があります。

### ローカルでのアプリケーションの実行

Administrateのデモアプリケーションは、他のRailsアプリケーションと同様に実行できます。

```
sh
bin/dev
```

これにより、`spec/example_app` で定義されたアプリケーションが起動します。

`/admin` にアクセスすると、ブラウザで `example_app` を表示できます。


## リポジトリ構造

* gemのソースコードは`app`と`lib`サブディレクトリに格納されています。

* デモアプリは`spec/example_app`の中にネストされています。

Railsの設定ファイルは、

新しい場所にあるアプリを認識するように変更されているため、

サーバーの実行やHerokuへのデプロイは正常に動作します。


## フロントエンドアーキテクチャ

このプロジェクトでは以下を使用しています。

* Sass
* [BEM] スタイルの CSS セレクタ（[namespaces] 付き）
* Autoprefixer
* SCSS-Lint（[stylelint] ([configuration](stylelint-config)) 付き）
* 様々な CSS 単位：
- `em`：タイポグラフィ関連の要素

- `rem`：コンポーネントの長さ

- `px`：境界線、テキストシャドウなど

- `vw`/`vh`：ビューポートに比例する長さ

[BEM]：http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/
[namespaces]：http://csswizardry.com/2015/03/more-transparent-ui-code-with-namespaces/
[stylelint]： https://stylelint.io

## アイコン

アイコンには[Feather][]を使用しています。



[Feather]: https://feathericons.com

## ラベル

課題とプルリクエストは、上位レベルのラベルで2段階に分類されます。

* `feature`: 未実装の新機能、
* `bug`: 実装済みの機能における不具合、
* `maintenance`: 周囲の変更に対応するためのメンテナンス

…さらに、より具体的なテーマのラベルは以下のとおりです。

* `namespacing`: 名前空間を持つモデル、
* `installing`: 初期設定、初回起動時の操作、ジェネレーター、
* `i18n`: 翻訳と多言語サポート、
* `views-and-styles`: administrateの外観と操作方法、
* `dashboards`: administrateにおけるフィールドの表示方法とデータ表示方法、
* `search`: モデルを通じた検索、
* `sorting`: ダッシュボード上の項目の並べ替え、
* `pagination`: 大量のデータを小さなページにどのように表示するかチャンク、
* `security`: 認証によるデータアクセス制御、
* `fields`: 新規フィールド、データの表示と編集、
* `models`: モデル、関連付け、および基となるデータの取得、
* `documentation`: Administrate の使い方、例、一般的な使用方法、
* `dependencies`: 依存関係に関する変更点または問題

## ドキュメント

ダッシュボードの外観、動作、およびコンテンツをカスタマイズするために、
ドキュメントを公開しています。

これらのガイドは、
git リポジトリの `docs` サブディレクトリに Markdown ファイルとして保存されています。

## 貢献

[CONTRIBUTING.md](/CONTRIBUTING.md) を参照してください。

RubyAdminPanel は、元々 Grace Youngblood によって作成され、現在は
Nick Charlton によってメンテナンスされています。多くの改善点やバグ修正は、[オープンソースコミュニティ](https://github.com/tuoc1226-maker/RubyAdminPanel/graphs/contributors)によって提供されました。

## ライセンス

RubyAdminPanelは中林青人によって作成されました。