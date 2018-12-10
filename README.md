# WordPressのテーマをカスタマイズする案件でサクッと環境作るときのnode-scriptサンプル

## 処理

* SASS(SCSS)コンパイル
* autoprefixer,CSS圧縮
* `.min.css`にリネーム
* browser-sync

### SASS(SCSS)コンパイル

`src/sass` -> `src/css`へコンパイル

SASSコンパイルでは圧縮ぜず、デバッグ用にとっておく

### autoprefixer,CSS圧縮

プレフィックス追加・CSS圧縮をして`src/css` -> `css`へコンパイル

### `.min.css`にリネーム

`.min.css`以外のファイルを`.min.css`にリネーム

### browser-sync

proxy機能を使う場合、`-s ./`を`-p [ドメイン名]`に変更する

`.local`ドメインを使うと遅くなるので注意！
`.dev`は自動でhttpsにリダイレクトされるので注意！

`.lo`やら適当なローカルドメインを使うこと。
（`hosts`の編集も忘れずに）