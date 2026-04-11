# 新歓2026 担当体験会（未整備）

2024 年度の新歓 HP・PF 担当体験会で使用するリポジトリです。

使用法については、[こちら](./docs/index.md)を参照してください。


## 以下未確認情報

srcファイル以下をすべてダウンロードしてください
ファイルの階層を変えないこと！！
使い始める前に以下をターミナルで実行してください

```
npx @tailwindcss/cli -i ./src/input.css -o ./src/output.css --watch
```

うまくいかないときは

```
npm install tailwindcss @tailwindcss/cli
```

を実行してみてください

- src/input.css

基本的には使いません
43 - 56 に新たに定義した class が入ってます。class 名からどのコンポーネントに対応しているか察してください（）

- src/output.css

基本的には使いません
TailWind CSS の class が入ってます

- src/section.html

メインで使っていくファイルです
新歓サイトの担当ページが再現してあります（カードなど一部デザインが変わっていますが担当体験会の内容上（あと少しめんどくさかったりして）なのであまり気にしないでください）

- src/images

画像が入っています
