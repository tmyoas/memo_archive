# GithubとIntelliJの連携
今まで面倒なことをしていたことに気付いたのでメモ。
IntelliJだけでCloneができるよ、という話。

## やりたいこと
新規リポジトリをGithub上に作り、IntelliJでProjectとして開く

## やりかた
### の前に
以下は実施済みの体
- Githubアカウントの作成
- 端末へのGitインストールと初期設定
  - 必要かは知らない
- IntelliJのインストール

### 本手順
1. Githubに新規リポジトリを作る
  1. 右上の+ -> New Repository
  2. Repository Name(とDescription)を入力
  3. "Initialize this..."にチェックを入れる
    1. これでREADME.mdを自動で作ってくれる
    1. gitはそのままだと空のディレクトリを管理できない&どうせ書くので作ってもらう
  4. Add .gitignore: NoneをJavaに変更
    1. .gitignoreを言語に応じて自動生成してくれる
    1. もちろんJavaでない場合は適宜選択
  5. Create Repositoryをクリック
2. Git Cloneを行う
  1. 作成したリポジトリのURLをコピー
    1. ブラウザからリポジトリのページに行くと、Clone or downloadからコピーできる
  1. IntelliJを起動
  1. File -> New -> Project from Version Control -> Gitを選択
  2. URL: にコピーしたURLをペースト
    1. Directory: は自動で設定されるが気に入らないときは適宜修正
  3. Cloneを選択
    1. 今のウインドウで開くか新しいウインドウで開くか聞かれるのでお好みで
3. 確認
  1. Gitコンソールから指定した上で指定したディレクトリに行くと、Git管理対象になっていることがわかる
