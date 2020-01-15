---
title: Sublime Merge 教程 - 合并  
tags: ["sublime-merge"]  
excerpt: Sublime Merge 教程 - 合并  
date: 2020-1-15  
---

# Sublime Merge 教程 - 合并 (git merge)  


### 合并分支  
![](https://raw.githubusercontent.com/floydawong/images/master/img/sublime-merge-merge-operate.png)  

假设有 2 个分支, 分别是 `develop` 和 `test` 分支. 现在我们想要把 `test` 分支的代码合并到 `develop` 分支. 操作步骤如下:  
1. 确认当前分支为 `develop`.  
2. 鼠标右键点击 `test`.  
3. 选择 `Merge test into delelop...`.  


### 合并时的参数  
![](https://raw.githubusercontent.com/floydawong/images/master/img/sublime-merge-merge-3-param.png)  
![](https://raw.githubusercontent.com/floydawong/images/master/img/sublime-merge-merge-2-param.png)  

- `--ff`: 默认方式 (fast-forward). 保留分支的提交记录, 但不会生成合并的提交记录.
- `--no--ff`: 不使用 fast-forward 方式合并, 保留分支的 commit 历史, 并生成一次合并的提交记录.  
- `--squash`: 使用 squash 方式合并, 把分支所有 commit 历史压缩为一次.  
- `--commit`: 默认方式. 参数使得合并后产生一个合并结果的 commit 节点. 该参数可以覆盖 --no-commit.  
- `--no-commit`: 参数使得合并后, 为了防止合并失败并不自动提交, 能够给使用者一个机会在提交前审视和修改合并结果.  


### 一图胜千言  
![](https://segmentfault.com/img/bVkJAj)  
![](https://segmentfault.com/img/bVkyHw)  
