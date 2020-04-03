---
title: [工作日志] Android 不同渠道配置不同的图标名字版本号等等  
tags: ["work", "android", "icon"]  
excerpt: [工作日志] Android 不同渠道配置不同的图标名字版本号等等  
date: 2020-4-3  
---

# [工作日志] Android 不同渠道配置不同的图标名字版本号等等  


1. 在 `AndroidManifest.xml` 文件中修改 `android:icon="${app_icon}"`  
2. 在 `build.gradle` 中添加 2 个属性.  
一个是 `productFlavors`  
一个是 `flavorDimensions`  

```gradle
apply plugin: 'com.android.application'

android {
    compileSdkVersion 26
    buildToolsVersion '27.0.3'
    lintOptions {
        checkReleaseBuilds false
        abortOnError false
    }
    defaultConfig {
        minSdkVersion 19
        targetSdkVersion 22
        versionCode 16
        versionName "2.0.0"
        ndk {
            abiFilters 'armeabi'
        }
    }
    buildTypes {
        debug {
            // ...
        }
        release {
            // ...
        }
    }
    lintOptions {
        checkReleaseBuilds false
        abortOnError false
    }
    sourceSets.main {
        jni.srcDirs = []
    }

    flavorDimensions "version"
    productFlavors {
        AAA {
            manifestPlaceholders = [app_icon: "@drawable/icon_aaa"]
        }

        BBB {
            manifestPlaceholders = [app_icon: "@drawable/icon_bbb"]
        }
    }
}

repositories{
    flatDir {
        dirs 'libs'
    }
}

dependencies {
    implementation fileTree(dir: 'libs', include: ['*.jar','*.aar'])
    // ...
}
```
