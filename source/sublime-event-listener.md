---
title: Sublime Text EventListener  
tags: ["Sublime", "EventListener"]  
excerpt: Sublime EventListener  
date: 2020-3-17  
---

# Sublime Text EventListener  


## 什么是`EventListener`  
> Note that many of these events are triggered by the buffer underlying the view, and thus the method is only called once, with the first view as the parameter.  


## 可以监听的事件  
| method | description |
| - | - |
| on_new(view) | |
| on_new_async(view) | |
| on_clone(view) | |
| on_clone_async(view) | |
| on_load(view) | |
| on_load_async(view) | |
| on_pre_close(view) | |
| on_close(view) | |
| on_pre_save(view) | |
| on_pre_save_async(view) | |
| on_post_save(view) | |
| on_post_save_async(view) | |
| on_modified(view) | |
| on_modified_async(view) | |
| on_selection_modified(view) | |
| on_selection_modified_async(view) | |
| on_activated(view) | |
| on_activated_async(view) | |
| on_deactivated(view) | |
| on_deactivated_async(view) | |
| on_hover(view) | |
| on_query_context(view) | |
| on_query_completions(view) | |
| on_text_command(view) | |
| on_window_command(window) | |
| on_post_text_command(view) | |
| on_post_window_command(window) | |




[Sublime API](http://www.sublimetext.com/docs/3/api_reference.html)
