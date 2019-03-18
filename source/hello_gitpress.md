---
title: Hello GitPress
tags: ["GitPress"]
excerpt: 个人简介
date: 2019-3-18
---

# Hello GitPress

GitPress的使用参照: [搭建个人GITPRESS博客](https://gitpress.io/@yangshijie/how-to-build-gitpress-blog)

## Tag的使用

```YAML
---
title: Front Matter Specifications
tags: ["GitPress", "GitPressHelp"]
excerpt: Explaination of front-matters, settings and default values supported by GitPress.
date: 2018-12-31
---
```

在每一个md文件前, 可以加入一个`yaml`的`Front-matter`, 他的参数有:  
- title
- tags
- excerpt
- date

其中`tags`貌似是全局共用的.   
```
https://gitpress.io/t/search_tag
```
替换`search_tag`, 可以检索到所有人为其标注的tag.  


## Todo

- CNAME的使用(目前我是创建了一个`gh-pages`分支, 通过html的跳转来实现的, 期待更好的方法)
- Sublime的插件(是否需要单独为其写一个插件, 还是整合到`GWNote`中, 需要思考一下)
