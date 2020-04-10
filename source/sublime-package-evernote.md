---
title: Sublime Package Evernote
tags: ["sublime", "evernote"]
excerpt: sublime package evernote
date: 2020-4-10
---

# Sublime Package Evernote
Evernote 是一个 Sublime 的插件, 作用是在 Sublime 中使用印象笔记.  


## 安装  
> http://packagecontrol.cn/packages/Evernote  
> http://packagecontrol.io/packages/Evernote  

通过 `Package Control` 安装, 搜索 `Evernote`.  

## 配置  
> https://github.com/bordaigorl/sublime-evernote/wiki/First-Use  

### 中国印象笔记用户(app.yinxiang.com)  

插件里面应用授权 (Reconfigure Authorization) 是面向 Evernote International 用户，  

如果你是中国印像笔记用户 (app.yinxiang.com) 用户，此插件同样适用， 只需做以下修改:  

  1. 到 <https://app.yinxiang.com/api/DeveloperToken.action> 登陆获取应用授权  
  2. 你将获得 Developer Token 和 NoteStore URL  
  3. 打开 sublime Evernote 插件设置文件 `Preferences > Package Settings > Evernote > Settings - User`  
  4. 将上面获取到的信息复制到对应的地方, 格式是：  
```json
{
    // 你的 NoteStore URL
    "noteStoreUrl":"http://app.yinxiang.com/shard/s44/notestore", 
    // 你的 Developer Token
    "token": "S=s44...6a51561c3" 
    }
```
  5. token 是以 `S=` 开头的一串字符串  
  6. noteStoreUrl 是一段 http 地址，但这里你需要手动将 `https` 替换成 `http`  
  7. 保存设置文件（你可能还需要重启你的 `Sublime Text`），尝试打开一个笔记确保你的印象笔记能正常工作了  


## 自定义快捷键  
在 `./AppData/Roaming/Sublime Text 3/Packages/User/Default (Windows).sublime-keymap` 中添加  
```
{"keys": ["ctrl+alt+e"], "command": "show_overlay", "args": {"overlay": "command_palette", "text": "Evernote:"} },
```

方便我们快速的打开 `Evernote` 的菜单.  
