# AI部活動 - GitHub Pages

このプロジェクトはGitHub Pagesを使用して公開されている静的Webサイトです。

## プロジェクト概要

- **技術スタック**: HTML5, CSS3
- **ホスティング**: GitHub Pages
- **デザイン**: モダンでレスポンシブなデザイン

## ファイル構成

```
AI_Bukatsu/
├── index.html          # メインページ
├── README.md           # このファイル
└── .gitignore          # Git除外設定
```

## GitHub Pagesで公開する手順

### 1. GitHubリポジトリの作成

1. GitHubにログインします
2. 右上の「+」アイコンをクリックし、「New repository」を選択
3. リポジトリ名を入力（例: `AI_Bukatsu`）
4. リポジトリを「Public」に設定（GitHub Pagesの無料プランではPublicリポジトリが必要）
5. 「Initialize this repository with a README」のチェックは外す（既にREADME.mdがあるため）
6. 「Create repository」をクリック

### 2. ローカルリポジトリのセットアップ

既にGitリポジトリが初期化されている場合は、以下のコマンドでリモートリポジトリを追加します：

```bash
git remote add origin https://github.com/[ユーザー名]/[リポジトリ名].git
git branch -M main
git push -u origin main
```

まだGitリポジトリが初期化されていない場合は、以下のコマンドを実行します：

```bash
git init
git add .
git commit -m "Initial commit: GitHub Pages setup"
git branch -M main
git remote add origin https://github.com/[ユーザー名]/[リポジトリ名].git
git push -u origin main
```

**注意**: `[ユーザー名]`と`[リポジトリ名]`は実際の値に置き換えてください。

### 3. GitHub Pagesの有効化

1. GitHubリポジトリのページにアクセス
2. 上部のメニューから「Settings」をクリック
3. 左側のサイドバーから「Pages」をクリック
4. 「Build and deployment」セクションの「Source」ドロップダウンを開く
5. **「Deploy from a branch」**を選択（「GitHub Actions」ではなくこちらを選択）
6. ブランチとフォルダの選択肢が表示されるので、以下を設定：
   - **Branch**: `main`を選択
   - **Folder**: `/ (root)`を選択
7. 「Save」をクリック

### 4. 公開URLの確認

数分後（通常1-2分）、以下のURLでWebサイトにアクセスできます：

```
https://[ユーザー名].github.io/[リポジトリ名]
```

例: `https://username.github.io/AI_Bukatsu`

### 5. 更新方法

Webサイトを更新するには：

1. ローカルでファイルを編集
2. 変更をコミットしてプッシュ：

```bash
git add .
git commit -m "Update website"
git push
```

3. 数分後に変更が反映されます

## カスタムドメインの設定（オプション）

独自ドメインを使用する場合：

1. リポジトリのルートに`CNAME`ファイルを作成
2. ファイルにドメイン名を記述（例: `example.com`）
3. DNS設定でCNAMEレコードを追加：
   - **Type**: CNAME
   - **Name**: `@` または `www`
   - **Value**: `[ユーザー名].github.io`

## トラブルシューティング

### サイトが表示されない

- GitHub Pagesの設定が正しいか確認（Settings > Pages）
- ブランチ名が`main`であることを確認
- 数分待ってから再度アクセスを試す（反映に時間がかかることがあります）

### 変更が反映されない

- ブラウザのキャッシュをクリア
- 数分待ってから再度確認
- GitHub Actionsのページでビルドエラーがないか確認

## ライセンス

このプロジェクトはMITライセンスの下で公開されています。
