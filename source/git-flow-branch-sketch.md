---
title: Git Flow 流入流出示意图
notebook: git
tags: ["git-flow", "branch"]
date: 2020-8-4  
---

## start feature branch  

```
master --------------------->
      \               
       develop ------------->
              \       /
            => feature <=
```

## start release branch  

```
master --------------\
      \               \
       develop ------------->
              \       /
            => release <=
```

## start bugfix branch  

```
master --------------------->
      \
       develop ------------->
              \      /
            => bugfix <=
```

## start hotfix branch  

```
       develop ------------->
      /        /
master -------/
      \      /
    => hotfix <=
```

## start support branch  
> - 只能从 master 分支 checkout  
> - 没有 finish, 可以 rebase  

```
       develop ------------->
      /        
master --------------------->
      \       
    => support <= ---------->
```
