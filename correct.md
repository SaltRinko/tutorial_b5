# 演習問題解答

## __初級問題__
### マスターブランチでコンフリクト祭り！！
頑張る


## __発展問題__

問0：masterブランチからchallengeブランチへ移動しなさい
（以下の問題もchallengeブランチで行う）

### reset
問1：コミットメッセージが「佐藤さんの要望」のコミットまでの変更内容を取り消しなさい（「佐藤さんの要望」のコミット自体は残す）

解答例
reset --hard HEAD~~~~...
reset --hard <佐藤さんの要望のコミットID>

問2：やはり、コミットメッセージが「森さんの要望」までを取り消す方がよかったため、そこまで戻しなさい（「森さんの要望」のコミット自体は残す）

解答例
reset --hard ORIG_HEAD
reset --hard HEAD~~~... or reset --hard <森さんの要望のコミットID>

### commit --amend
問3：「森さんの要望」というコミットメッセージを「林さんの要望」に直しなさい

解答例
git commit --amend

### revert
問4：コミットメッセージが「吉田さんの要望」というコミットのみを取り消しなさい。ただし、コミットを取り消したというログは残しておくこと。


解答例
git revert <「吉田さんの要望」のコミットID>

### cherry-pick
問5：コミットメッセージが「加藤さんの要望」のコミットのみをmasterブランチに反映させなさい。コンフリクトが起きた場合はchallengeブランチ側の編集内容を優先すること。

解答例
git checkout master 
git cherry-pick <「加藤さんの要望」のコミットID>
※コンフリクトさせるようにmasterのコードを書き加えておく
コンフリクトを解消してコミット

### rebase -i (コミットをまとめる)
問6：コミットメッセージが「木村さんの要望」となっているコミットを全て1まとめにし、コミットメッセージを「木村さんの全要望」としなさい。また、まとめたコミットの位置は一番最後の「木村さんの要望」の所にまとめておくこと。（佐藤さんの要望の1つ前に位置する）

解答例
git rebase -i HEAD~...
そして木村さん
からのpickをsquash(s)にして保存
その後コミットメッセージを編集し忘れていたら
git commit --amend

メモ、git rebase --abortでrebaseを中止できる


### rebase -i (コミットを編集する)
問7：
問6でまとめたコミットの内容を編集しなさい。
編集内容：「木村 翼」さんの数値に100加算する。

解答例
git rebase -i HEAD~...
該当箇所のpickをeditに書き換え、編集
git add .
git commit --amend（変更を保存）
git rebase --continue 

### merge
問8：以上のchallengeブランチでのコミット履歴を残したまま、masterへmergeせよ。


解答例
git checkout master
git merge --no-ff challenge
