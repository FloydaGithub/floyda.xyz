---
title: Sublime Merge 使用规范  
tags: ["sublime-merge"]  
excerpt: Sublime Merge 使用规范  
date: 2020-3-27  
---

# Sublime Merge 使用规范  

## Git Flow  
- master  
主分支: 正式版本.  
- develop  
开发分支: 所有代码都汇聚在这个分支.  
- feature  
一个新功能, 一个 feature 分支.  
- release  
要发布一个新版本时, 创建此分支. 其他分支继续开发后续功能.  
- bugfix  
master 分支有 bug 需要修复时, 创建此分支. 代码从 master 分支 clone, 合并到 master.  
- hotfix  
- support  

## 心得  
- 无论分支从哪里出来, 回到哪里. 最末端的分支用 add/commit 的方式提交代码. 其他分支都用合并的方式.  
- 简单的说, master 和 develop 分支都用 merge, 其他分支用 add/commit  
