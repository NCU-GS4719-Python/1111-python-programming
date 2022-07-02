## 備註

如果出現錯誤，希望大家指出，提出PR編修！

## 目錄

* [1. git 與 svn 的區別在哪裡？](#1-git-與-svn-的區別在哪裡)
* [2. 經常使用的 git 命令？](#2-經常使用的-git-命令)
* [3. git pull 和 git fetch 的區別](#3-git-pull-和-git-fetch-的區別)
* [4. git rebase 和 git merge 的區別](#4-git-rebase-和-git-merge-的區別)

### 1. git 與 svn 的區別在哪裡？
   ```
   git 和 svn 最大的區別在於 git 是分散式的，而 svn 是集中式的。因此我們不能在
   離線的情況下使用 svn。如果伺服器出現問題，我們就沒有辦法使用 svn 來提交我們
   的程式碼。

   svn 中的分支是整個版本庫的複製的一份完整目錄，而 git 的分支是指標指向某次提交，
   因此 git 的分支創建更加開銷更小，並且分支上的變化不會影響到其他人。svn 的分支
   變化會影響到所有的人。
   ```

### 2. 經常使用的 git 命令？
   ```
   git init                     // 新建 git 程式碼庫
   git add                      // 添加指定檔到暫存區
   git rm                       // 刪除工作區檔，並且將這次刪除放入暫存區
   git commit -m [message]      // 提交暫存區到倉庫區
   git branch                   // 列出所有分支
   git checkout -b [branch]     // 新建一個分支，並切換到該分支
   git status                   // 顯示有變更的檔
   ```

### 3. git pull 和 git fetch 的區別 
   ```
   git fetch 只是將遠端倉庫的變化下載下來，並沒有和本地分支合併。

   git pull 會將遠程倉庫的變化下載下來，並和當前分支合併。

   git pull = git fetch + git merge
   ```
   

### 4. git rebase 和 git merge 的區別
   ```
   git merge 和 git rebase 都是用於分支合併，關鍵在 commit 記錄的處理上不同。

   git merge 會新建一個新的 commit 物件，然後兩個分支以前的 commit 記錄都指向
   這個新 commit 記錄。這種方法會保留之前每個分支的 commit 歷史。

   git rebase 會先找到兩個分支的第一個共同的 commit 祖先記錄，然後將提取當前分
   支這之後的所有 commit 記錄，然後將這個 commit 記錄添加到目標分支的最新提交
   後面。經過這個合併後，兩個分支合併後的 commit 記錄就變為了線性的記錄了。
   ```

## 資料來源：
1. [Front-End-Interview-Notebook 常用的工具知識總結](https://github.com/CavsZhouyou/Front-End-Interview-Notebook/blob/master/%E5%B7%A5%E5%85%B7/%E5%B7%A5%E5%85%B7.md)
