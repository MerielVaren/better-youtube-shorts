# 更好的 Youtube Shorts

## 為 youtube shorts 提供了更多功能，包括

- 可自動跳轉到對應video界面
- 快捷鍵 alt + w ，可手動打開shorts對應的video界面，如[https://www.youtube.com/shorts/9wRiG-A7K8A](https://www.youtube.com/shorts/9wRiG-A7K8A)，本腳本可打開[https://www.youtube.com/watch?v=9wRiG-A7K8A](https://www.youtube.com/watch?v=9wRiG-A7K8A)，在影片界面打開當前shorts
- 進度條（含時間顯示，可以拖動）
- 音量控制（含音量顯示）
- 自動滾動控制

### 腳本推薦：[Tabview Youtube](https://greasyfork.org/zh-CN/scripts/428651-tabview-youtube)，最大的優點是能一邊看影片一邊看評論而不用來回的上下滾動，非常好用

## 腳本特點

- <h3>沒有 setInterval 造成的性能問題，使用requestAnimationFrame，並且只渲染需要的部分，大大減少了性能消耗</h3>

## 最佳化點

- <h3>解決在有廣告攔截插件及擴展的情況下該插件失效的問題</h3>
- <h3>最佳化載入速度</h3>
- <h3>解決從其他頁面（如用戶首頁，首頁的shorts欄等）進入的shorts不載入Better Youtube Shorts界面的問題</h3>

## 腳本選項（在Tampermonkey / ViolentMonkey菜單中）

### 1. 選項 "Shorts Auto Switch To Video"

- off: 不自動切換到影片界面
- on: 自動切換到影片界面

### 2. 選項 "Loop Playback" （該選項在關閉autoscroll後才有效果，否則優先自動滾動）

- off: 播放完一個影片後停止
- on: 影片播放完會自動無限循環

### 3. 選項 "Continue From Last Checkpoint"

- off: shorts的默認邏輯，每個shorts從0s開始播放
- temporary: 記憶每個shorts最後的位置，再一次回到這個shorts時從上一次離開的位置繼續（每一次網頁刷新，這些記憶被都會重設）
- permanent：網頁刷新不會再重設這些記憶

### 4. 選項 "Constant Volume"

- off: 使用youtube對shorts使用的默認音量邏輯，每個影片都有自己的音量
- on: 所有瀏覽的shorts都採用用戶在音量條上設置的音量

### 5. 選項 "Open Watch In Current Tab"（該選項在ShortsAutoSwitchToVideo為off，即停留在shorts界面時才有效）

- off: 在新標籤頁打開當前shorts對應的watch界面
- on: 在當前標籤頁打開shorts對應的watch界面

### 6. 選項 "Double Click To Fullscreen"

- off: 關閉雙擊全螢幕（以便相容其他插件在shorts上的雙擊操作）
- on: 打開雙擊全螢幕

### 7. 選項 "Operation Mode"

- Video (Yotube影片採用的快捷鍵，加上shift控制滾動影片)
  - 上/下箭頭 - 音量減小/增大
  - 左/右箭頭 - 後退/前進
  - Shift+左/Shift+右 - 上一個/下一個影片
  - Shift+上/Shift+下 - 上一個/下一個影片
  - 空格 - 播放/暫停
  - 雙擊影片 - 全螢幕
  - 回車 - 全螢幕
  - alt + w - 打開shorts對應的影片界面
- Shorts (Youtube Shorts採用的快捷鍵，加上shift控制音量)
  - 上/下箭頭 - 上一個/下一個影片
  - 左/右箭頭 - 後退/前進
  - Shift+左/Shift+右 - 音量減小/增大
  - Shift+下/Shift+上 - 音量減小/增大
  - 空格 - 播放/暫停
  - 雙擊影片 - 全螢幕
  - 回車 - 全螢幕
  - alt + w - 打開shorts對應的影片界面