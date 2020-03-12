# git-learn

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
（git remote add 分支名稱 專案位置）
專案位置-兩種不同管道
https：每次要把東西往上推時，都會問GitHub帳密
SSH：不用每次輸入帳號密碼，要先設定SSH Key。分私鑰、公鑰兩種，私鑰絕對不能給，公鑰放在外面(GitHub)上，當需要推專案時，公鑰私鑰對起來，就可以判定你是不是擁有者。私鑰不能弄掉，記得要備份。


git remote -v 查分支、專案狀態？
![](https://i.imgur.com/HhNG6ql.png)

git push -u xxx master
-u 做一次遠端跟本地連結
未來只要 git push 就可以直接...???

生成SSH Key
$ssh-keygen



![](https://i.imgur.com/WlJiAfG.png)
![](https://i.imgur.com/w376ZRy.png)
![](https://i.imgur.com/F7b6qtw.png)




![](https://i.imgur.com/aTxZa0L.png)
