---
theme: seriph
background: ./assets/bg.webp
title: Frontend Performance Tuning
info: |
  ## Frontend Performance Tuning
  分析常見的前端效能優化方式

class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
duration: 45min
---

# Frontend Performance Tuning

## 前端效能調教指南

<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  Press Space for next page <carbon:arrow-right />
</div>


--- 

# TT

<div class='border'>AA</div>
<mdi-account-circle /> 


## 常見的分析方式

介紹進行效能分析的主要工具和方法


---

## Chrome DevTools - Performance Tab

### 開啟 Performance 面板

1. 打開 Chrome DevTools (F12 或 Cmd+Option+I)
2. 切換到 **Performance** 標籤頁
3. 點擊紅色錄製按鈕開始記錄
4. 進行頁面交互操作
5. 點擊停止錄製按鈕

### 主要分析指標

- **FCP (First Contentful Paint)**: 第一個內容繪製時間
- **LCP (Largest Contentful Paint)**: 最大內容繪製時間
- **TTI (Time to Interactive)**: 互動時間
- **TBT (Total Blocking Time)**: 總阻塞時間

---

## Performance Tab 詳細分析

### 時間軸視圖

```
┌─────────────────────────────────────────────┐
│ 幀率圖表 (Frame Rate)                        │
├─────────────────────────────────────────────┤
│ 主執行緒活動 (Main Thread Activity)          │
│ ├─ 黃色: JavaScript 執行                    │
│ ├─ 紫色: Rendering                         │
│ └─ 綠色: Painting                          │
├─────────────────────────────────────────────┤
│ 資源載入時間軸 (Network Timeline)           │
└─────────────────────────────────────────────┘
```

---

## 分析步驟

1. **識別長任務 (Long Tasks)**
   - 尋找超過 50ms 的 JavaScript 執行任務
   - 這些會導致頁面卡頓

2. **檢查渲染效能**
   - 觀察是否有過多的 Layout 和 Paint 操作
   - 使用 Rendering 分析找出性能瓶頸

3. **記錄自訂測量**
   - 使用 `console.time()` 和 `console.timeEnd()`
   - 標記關鍵操作的開始和結束

4. **導出和共享**
   - 將分析結果導出為 JSON 檔案
   - 便於與團隊討論

---

layout: center
class: text-center
---

# 開始優化你的應用！
