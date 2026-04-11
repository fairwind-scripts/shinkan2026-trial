srcファイル以下をすべてダウンロードしてください
ファイルの階層を変えないこと！！

- src/input.css

基本的には使いません
43 - 56 に新たに定義した class が入ってます。class 名からどのコンポーネントに対応しているか察してください（）
今回使われていなかった TailWind CSS の class を使いたくなったら

```
npx @tailwindcss/cli -i ./src/input.css -o ./src/output.css --watch
```

をターミナルで実行してください。うまくいかないときは

```
npm install tailwindcss @tailwindcss/cli
```

を実行してみてください

- src/output.css

基本的には使いません
TailWind CSS の class が入ってます

- src/section.html

メインで使っていくファイルです
新歓サイトの担当ページが再現してあります（カードなど一部デザインが変わっていますが担当体験会の内容上（あと少しめんどくさかったりして）なのであまり気にしないでください）

- src/images

画像が入っています
