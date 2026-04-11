# 新歓2026 担当体験会

## 環境構築

以下、macOS では Homebrew を使用すると便利ですが、Homebrew のインストール方法は割愛します。  
PATH の設定などが必要な場合もありますが、ターミナルに表示されるメッセージに従えば基本的には問題ありません。

---

## 1. Docker Desktop のインストール

[公式サイト](https://docs.docker.com/desktop/)を参考に Docker Desktop をインストールしてください。

- [macOS](https://docs.docker.com/desktop/setup/install/mac-install/)
- [Windows](https://docs.docker.com/desktop/setup/install/windows-install/)

macOS の場合、Homebrew でもインストールできます。

```bash
brew install --cask docker
```

次のコマンドでバージョンが表示されれば、インストールは完了です。

```bash
docker --version
```

インストールが完了したら、Docker Desktop を起動してください。

---

## 2. VS Code のインストール

公式サイトを参考に VS Code をインストールしてください。

macOS の場合、Homebrew でもインストールできます。

```bash
brew install --cask visual-studio-code
```

インストールが完了したら、VS Code を起動してください。

なお、以下の表記は [Japanese Language Pack for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=MS-CEINTL.vscode-language-pack-ja) がインストールされていることを前提としています。

---

## 3. `code` コマンドのインストール

VS Code を起動したら、「表示」→「コマンド パレット」を選択し、  
`Shell Command: Install 'code' command in PATH` を実行してください。

コマンドパレットは、`Ctrl + Shift + P`（macOS では `Cmd + Shift + P`）でも開けます。  
ウィンドウ上部の検索バーをクリックして `>` を入力して開く方法でも OK です。

これで、ターミナルから `code` コマンド（VS Code を起動するコマンド）が使えるようになります。

---

## 4. Git のインストール

[公式サイト](https://git-scm.com/book/ja/v2/%E4%BD%BF%E3%81%84%E5%A7%8B%E3%82%81%E3%82%8B-Git%E3%81%AE%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB)を参考に Git をインストールしてください。

macOS の場合、Homebrew でもインストールできます。

```bash
brew install git
```

次のコマンドでバージョンが表示されれば、インストールは完了です。

```bash
git --version
```

---

## 5. リポジトリのクローン

次のコマンドで、このリポジトリをクローンしてください。

```bash
git clone https://github.com/fairwind-scripts/shinkan2026-trial.git
```

クローンしたら、次のコマンドでディレクトリを移動してください。

```bash
cd shinkan2026-trial
```

次のコマンドで VS Code でこのリポジトリを開いてください。

```bash
code .
```

---

## 6. Dev Containers 拡張機能のインストール

VS Code でこのリポジトリを開いたら、拡張機能パネルを開き、`Dev Containers` をインストールしてください。

---

## 7. Dev Container で開く

ウィンドウ左下の `><` のようなアイコンをクリックし、「コンテナーで再度開く」を選択してください。

初回はコンテナーの作成に少し時間がかかります。  
このリポジトリでは、コンテナー作成後に `pnpm install` が自動で実行されます。

---

## 8. 開発の開始

このリポジトリは、`HTML + Tailwind CSS` でページを作る構成です。  
編集時は、以下の 2 つを使います。

### 8-1. Tailwind CSS の監視ビルド

ターミナルで次を実行してください。

```bash
pnpm dev
```

これで `src/input.css` の変更が `src/output.css` に反映され続けます。

### 8-2. HTML のプレビュー

1. `src/section.html` を開く
2. 右上の虫眼鏡付きのアイコンをクリックする

URL は環境によって多少異なりますが、例としては次のようになります。

```text
http://127.0.0.1:3000/src/section.html?vscode-livepreview=true
```

ページ上部に青背景の「担当ってなに？」が表示されれば、環境構築は成功です。

---

## 9. よくある詰まりポイント

- `docker --version` が通らない: Docker Desktop の起動とターミナル再起動を試す
- `pnpm` が使えない: コンテナー内で開けているか確認する（右下のステータスに `Dev Container` 表示があるか）
- CSS が反映されない: `pnpm dev` が実行中か確認する
- ページが開けない: Live Prevuew が起動しているか、ポート（通常 3000）がフォワードされているか確認する
