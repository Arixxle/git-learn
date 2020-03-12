# git-learn
### 線上編輯測試 0312 12:15
###### tags: `self`
# 2020-03-12 
:::info
- 錄影作業練習，目的在於了解大家卡關的地方，也是在訓練大家“解說”的能力，這在未來的面試很有用，科技業的面試，常會利用白板題，來測驗你思考與解說的能力。
:::

# GitHub
GitHub G & H 是大寫
相同的服務：GitLab/Bitbucket
開發這最好的履歷-血淋淋的戰場

開帳號
建立repository
![](https://i.imgur.com/DFNNdqW.png =300x)

按照提示，選擇對應的指令
![](https://i.imgur.com/SFOYa6V.png)

## 設定遠端節點

git remote add origin git@github.com:Arixxle/git-learn.git
（git ==remote== add 分支名稱(可自訂) 專案位置）
專案位置-兩種不同管道
https：每次要把東西往上推時，都會問GitHub帳密
SSH：不用每次輸入帳號密碼，要先設定SSH Key。分私鑰、公鑰兩種，私鑰絕對不能給，公鑰放在外面(GitHub)上，當需要推專案時，公鑰私鑰對起來，就可以判定你是不是擁有者。私鑰不能弄掉，記得要備份。

$git remote rm origin 刪除遠端分支（當你想改http/ssh節點時）


git remote -v 分支在遠端的位置
![](https://i.imgur.com/HhNG6ql.png)



生成SSH Key
$ ssh-keygen

![](https://i.imgur.com/WlJiAfG.png)

把id_rsa.pub（公鑰）用$cat 印出來，把內容貼到你要使用的服務中，allow write access
![](https://i.imgur.com/w376ZRy.png)

生成成功，接著就可以去push專案了
![](https://i.imgur.com/F7b6qtw.png)


git push -u origin master
-u 做一次遠端跟本地連結
未來只要 git push 就會記憶你最近用過的一次，去找對應的分支，把檔案推上去。

![](https://i.imgur.com/aTxZa0L.png)


git push origin master
git push origin master:master(完整版)
![](https://i.imgur.com/AT5PZTq.png)

git push origin master:cat
我要把本地的master分支推網origin這個遠端節點，並形成`cat`分支

## 刪除遠端分支
$ git push origin :cat
我要把本地的`無`master分支推網origin這個遠端節點，並形成`cat`分支＝刪除遠端分支



二階段驗證，使帳號更安全
![](https://i.imgur.com/kL0MvPN.png)


## Pull
$ git fetch origin master(抓)
![](https://i.imgur.com/I3sAizJ.png)
會比對線上與本地檔案，把本地沒有的，拉下來並新增一個origin/master的新分支(在master後)

$ git merge origin/master(合併)

$ git pull origin master(抓+合併)
$ git pull = git fetch + git merge
![](https://i.imgur.com/DDucFVE.png)

## 複製
$ git clone
會把整個專案`複製`一份下來，但不會做更新專案的動作
