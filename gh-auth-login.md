# GitHub CLI (gh) の HTTPS ログイン手順

このファイルでは、`gh auth login` を使って HTTPS で GitHub にログインする方法を説明します。

## 1. GitHub CLI のインストール

macOS では Homebrew が使えます。

```bash
brew install gh
```

## 2. GitHub CLI でログイン

ターミナルで以下を実行します。

```bash
gh auth login
```

### 3. 設定内容の選択

対話形式の質問に対して、以下のように選択します。

- `GitHub.com` を選択
- `HTTPS` を選択
- `Login with a web browser` を選択
- ブラウザが開いたら GitHub にログインし、認証を許可する

## 4. ログイン確認

ログインが成功したら、次のコマンドで認証状態を確認します。

```bash
gh auth status
```

`Logged in to github.com account <あなたのアカウント名>` が表示されれば成功です。

## 5. 以降の Git 操作

ログイン後は通常の HTTPS リモートを使って `git push` できます。

```bash
git push -u origin <ブランチ名>
```

## 6. 注意

- `gh auth login` でログインするアカウントは、push したいリポジトリへのアクセス権が必要です。
- ローカルの `user.name` / `user.email` はリポジトリごとに設定できます。

```bash
git config user.name "あなたのGitHubユーザー名"
git config user.email "あなたのメールアドレス"
```
