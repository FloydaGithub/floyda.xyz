---
title: Android 音频焦点  
tags: ["Android", "audio"]  
excerpt: Android 音频焦点  
date: 2020-3-19  
---

# Android 音频焦点  
> Doc: [管理音频焦点](https://developer.android.com/guide/topics/media-apps/audio-focus.html)  
> 两个或两个以上的 Android 应用可同时向同一输出流播放音频。系统会将所有音频流混合在一起。虽然这是一项出色的技术，但却会给用户带来很大的困扰。为了避免所有音乐应用同时播放，Android 引入了 “音频焦点” 的概念。 一次只能有一个应用获得音频焦点。  
>  
> 当您的应用需要输出音频时，它需要请求获得音频焦点，获得焦点后，就可以播放声音了。不过，在您获得音频焦点后，您可能无法将其一直持有到播放完成。其他应用可以请求焦点，从而占有您持有的音频焦点。如果发生这种情况，您的应用应暂停播放或降低音量，以便于用户听到新的音频源。  
>  
> 音频焦点采用合作模式。我们建议应用遵守音频焦点准则，但系统不会强制执行这些准则。如果应用想要在失去音频焦点后继续大声播放，系统无法阻止它。这是一种不好的体验，用户很可能会卸载具有这种不良行为的应用。  

---

**当我们启动游戏, 有其他的音频正在播放时, 我们需要将其关闭.**  
具体的办法有很多, 我选择了一个比较稳妥的方法, 就是申请一个新的焦点给游戏.  
其他App就失焦了, 声音或暂停或停止, 这个看它的处理方式.  


其代码如下:  
```Java
    AudioManager audioManager = (AudioManager) context.getSystemService(Context.AUDIO_SERVICE);
    AudioManager.OnAudioFocusChangeListener afChangeListener;

    ...
    // Request audio focus for playback
    int result = audioManager.requestAudioFocus(afChangeListener,
                                 // Use the music stream.
                                 AudioManager.STREAM_MUSIC,
                                 // Request permanent focus.
                                 AudioManager.AUDIOFOCUS_GAIN);

    if (result == AudioManager.AUDIOFOCUS_REQUEST_GRANTED) {
        // Start playback
    }
```  

---

### 需要调用这段代码的地方
- 游戏启动时, 主动让其他音频失焦.  
- 在游戏切后台时, 也要再次调用此方法.  
