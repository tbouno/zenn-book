# zenn-book

Zennの記事と本をGitHubで管理するためのリポジトリです。

## セットアップ

この環境では、Nixで管理されているNode.js/npmを使用します。

```sh
npm ci
```

## コンテンツを作成する

```sh
# 記事を作成
npm run new:article

# 本を作成
npm run new:book
```

スラッグなどのオプションは `--` の後に指定できます。

```sh
npm run new:article -- --slug my-first-article
```

記事は `articles/`、本は `books/` で管理します。

## プレビューする

```sh
npm run preview
```

起動後、ブラウザで <http://localhost:8000> を開きます。

## ZennとGitHubを連携する

1. [Zennのデプロイ設定](https://zenn.dev/dashboard/deploys)を開く
2. GitHubリポジトリ `tbouno/zenn-book` を連携する
3. Zennのリポジトリ設定で、デプロイ対象ブランチを `main` にする
4. 変更を `main` へpushすると、Zennへの同期が自動で開始される

GitHub Appの権限設定では `Only select repositories` を選び、このリポジトリだけを許可してください。

記事や本は最初は非公開で作成されます。公開する場合は、Markdownのfrontmatterにある `published` を `true` に変更してからpushします。

## 公式ドキュメント

- [Zenn CLIをインストールする](https://zenn.dev/zenn/articles/install-zenn-cli)
- [ZennとGitHubリポジトリを連携する](https://zenn.dev/zenn/articles/connect-to-github)
