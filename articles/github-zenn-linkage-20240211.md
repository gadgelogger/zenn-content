---
title: "Module 'Nuke' has no member named 'loadImage'になってブチ切れてる人へ（俺）"
emoji: "🐷"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: [Swift,iOS,Nuke,Xcode]
published: true
---


# 【背景】

https://mo-gu-mo-gu.com/ios-qiita-client-tutorial-api/

SwiftとUiKitの練習でこの記事のアプリを作ってみっかーと思ったら途中で詰んだので共有。
どうやらNukeの更新でNuke.loadImageがなくなってしまった模様。

ネットで調べてもあまり情報が無いため、メモ代わりにここに書いておく。

# ダメな書き方
```
Nuke.loadImage(with: ***, into: ***)
```

これだと
Module 'Nuke' has no member named 'loadImage'
となる。


# イケる書き方


### その１

```
import Nuke
import NukeExtensions //コレ追加
```
importでNukeに加えて"NukeExtensions"ってやつを追加

### その２
```
loadImage(with: ****, into: ***)
```

この書き方をする。そしたら動いたわ。
