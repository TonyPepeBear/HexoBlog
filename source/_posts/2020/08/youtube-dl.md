---
title: youtube-dl
date: 2020-08-31 16:17:17
tags:
    - youtube
    - youtube-dl
    - command
    - mac
---

`youtube-dl` 是強大的 Youtube 下載器，用簡單的指令就可以下載影片或音樂，唯一的缺點就是沒有介面，只能指令。

<!-- more -->

## Mac 安裝 youtube-dl

執行下面指令，安裝 `youtube-dl` 和 `ffmpeg`

``` bash
brew install youtube-dl
brew install ffmpeg
```

若還沒有安裝 Homebrew 請先自行搜尋安裝。

## 簡易下載

先進入到要存放下載檔案的資料夾，我這裡是選擇放到影片資料夾中

``` bash
cd Movies/
```

輸入下載指令，並將指令中的 `<LINK>` 換成要自己要下載的 youtube 連結

``` bash
youtube-dl <LINK>
```

## 轉檔成 mp4

預設下載的檔案可能不是 `mp4` 的格式，可以用 `ffmpeg` 轉換成 `mp4`

``` bash
youtube-dl -f mp4 <LINK>
```

## 下載較大的影片

預設下載的可能不是最高畫質的影片，先用指令把所有可下載的格式顯示出來

``` bash
youtube-dl -F <LINK>
```

這時會顯示出所有可以下載的影片解析度跟音檔，下載時記得影片的編號要在音檔之前，最後將檔案合併並輸出為 `mp4`

``` bash
youtube-dl -f "編號一+編號二" LINK --merge-output-format mp4
```

## 下載音樂

用 `-x` 參數表示要下載音樂，`--audio-format` 指定要輸出的檔案類型

``` bash
youtube-dl -x --audio-format mp3 <LINK>
```

### 在音訊檔中加入其他資料

* `--embed-thumbnail`：在輸出檔案中的專輯封面加入原影片的縮圖
* `—-add-metadata`：加入影片資訊
