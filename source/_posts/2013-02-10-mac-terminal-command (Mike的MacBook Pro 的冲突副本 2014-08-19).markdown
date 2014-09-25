---
layout: post
title: "Mac OS 通过终端Terminal开启各种隐藏功能"
date: 2013-02-10 22:50
comments: true
categories: mac
---

####显示隐藏文件
```
defaults write com.apple.finder AppliShowAllFiles TRUE

killall Finder
```

####显示文件路径
```
defaults write com.apple.finder _FXShowPosixPathInTitle -bool YES
```

####完全禁止Dashboard功能
```
defaults write com.apple.dashboard mcx-disabled -boolean YES
killall Dock
```

####开启 Quick Look 里的选中、复制功能
```
defaults write com.apple.finder QLEnableTextSelection -bool TRUE;killall Finder
```
