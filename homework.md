# Git / GitHub講座 宿題

## 目的

CLIでGitの基本操作を行い、GitHubブラウザでPull Requestを作成する流れを体験します。

この宿題では、GitHub上の練習用リポジトリを自分のPCにcloneし、ファイルを追加して、commit・push・Pull Request作成まで行います。

---

## 使用するもの

* GitHubブラウザ
* ターミナル、またはVS Codeのターミナル
* VS Code

---

## やること

1. GitHubで `git-github-practice` リポジトリを開く
2. CodeボタンからHTTPS URLをコピーする
3. ターミナルでリポジトリをcloneする
4. 自分用のブランチを作成する
5. `foods` フォルダに自分のファイルを作成する
6. VS Codeでファイルを編集する
7. CLIで変更内容を確認する
8. CLIで変更をaddする
9. CLIでcommitする
10. GitHubへpushする
11. GitHubブラウザでPull Requestを作成する
12. Pull RequestのURLを提出する

---

## ファイル名

自分に割り振られた番号で作成してください。

例：

* user-01 の人：`foods/user-01.md`
* user-02 の人：`foods/user-02.md`
* user-03 の人：`foods/user-03.md`

---

## ブランチ名

自分に割り振られた番号でブランチを作成してください。

例：

* user-01 の人：`feature/user-01-food`
* user-02 の人：`feature/user-02-food`
* user-03 の人：`feature/user-03-food`

---

## 作成するファイルの内容

以下の形で、自分の好きな食べ物について書いてください。

```md
# 好きな食べ物

## 食べ物
カレー

## 好きな理由
いろいろな具材を入れられて、味の種類も多いからです。

## ひとこと
辛すぎないカレーが好きです。
```

名前や個人情報は書かなくてOKです。

## 公開リポジトリでの注意

このリポジトリは講座用にPublicで作成されています。

以下は書かないでください。

- 本名
- 住所
- 電話番号
- メールアドレス
- SNSアカウント
- 学校名や事業所名
- その他、個人が特定される情報

課題では、好きな食べ物だけを書いてください。

---

## 補足

このリポジトリはPublicでも、pushできるのは権限を付与された人だけです。

講座では、受講者をCollaboratorとして招待したうえで、自分用のブランチにpushします。

---

## コマンド例

以下は `user-01` の人の例です。
自分の番号に置き換えて実行してください。

```bash
git clone https://github.com/あなたのユーザー名/git-github-practice.git
cd git-github-practice
git switch -c feature/user-01-food
```

VS Codeで、以下のファイルを作成します。

```txt
foods/user-01.md
```

ファイルを作成・編集したら、ターミナルで以下を実行します。

```bash
git status
git add foods/user-01.md
git commit -m "好きな食べ物を追加"
git push -u origin feature/user-01-food
```

---

## Pull Request作成

pushが終わったら、GitHubブラウザで `git-github-practice` リポジトリを開きます。

画面に `Compare & pull request` が表示されたら押します。

表示されない場合は、`Pull requests` タブから `New pull request` を押し、自分のブランチを選びます。

---

## Pull Requestタイトル

Pull Requestのタイトルは、以下の形にしてください。

例：

```txt
user-01の好きな食べ物を追加
```

自分の番号に置き換えてください。

例：

* `user-01の好きな食べ物を追加`
* `user-02の好きな食べ物を追加`
* `user-03の好きな食べ物を追加`

---

## 提出条件

作成したPull RequestのURLを提出してください。

---

## 注意点

* `main` ブランチに直接変更しないこと
* 他の人のファイルを編集しないこと
* ファイル名は半角英数字にすること
* commitしただけではGitHubに反映されません。pushが必要です
* pushしただけでは本体に取り込まれません。Pull Requestが必要です
* エラーが出た場合は、画面を閉じずにスクリーンショットを撮ってください

---

## 困ったとき

以下を確認してください。

* GitHubにログインできているか
* 正しいリポジトリを開いているか
* 自分のブランチで作業しているか
* 自分に割り振られたファイル名になっているか
* `git status` で現在の状態を確認したか

分からない場合は、エラー画面やターミナルの表示をそのまま共有してください。
