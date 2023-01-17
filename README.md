# Git入門演習問題
## 状況
ファイル共有の演習は完了
## 課題
演習問題チャプターでダウンロードしたファイルをGitHubに共有することができなかったため、チャプター03「ファイルやディレクトリの共有」でダウンロードしたファイルを代わりに共有した
### 試した内容
① チャプター03「ファイルやディレクトリの共有」で行なった手順通りCLIを操作を行う

② pushコマンドを送ると以下のエラーが表示
```
! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/kinamina/practice_git.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```
③ 解決方法をググって「pull」や「remote」コマンドで再度試したが、上記または下記の表示が出る
```
On branch main
nothing to commit, working tree clean
```
④ 代わりにチャプター03「ファイルやディレクトリの共有」でダウンロードしたファイルで試したところGitHub共有ができた

## コマンド詳細
```
kina.mina.@minamisawanamanarinoMacBook-Pro coachtech_2 % git init
Reinitialized existing Git repository in /Users/kina.mina./Desktop/coachtech_2/.git/
kina.mina.@minamisawanamanarinoMacBook-Pro coachtech_2 % git add -A         
kina.mina.@minamisawanamanarinoMacBook-Pro coachtech_2 % git remote add origin https://github.com/kinamina/practice_git.git
error: remote origin already exists.
kina.mina.@minamisawanamanarinoMacBook-Pro coachtech_2 % git remote rm origin
kina.mina.@minamisawanamanarinoMacBook-Pro coachtech_2 % git remote add origin https://github.com/kinamina/practice_git.git
kina.mina.@minamisawanamanarinoMacBook-Pro coachtech_2 % git push -u origin main
To https://github.com/kinamina/practice_git.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/kinamina/practice_git.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
kina.mina.@minamisawanamanarinoMacBook-Pro coachtech_2 % ls
index.html	style.css
```
