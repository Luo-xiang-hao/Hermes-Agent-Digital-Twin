# 📅 2026-09-19｜Phase 1-1 基礎 Agent 建置

## 🎯 今日目標

原本想照著老師的 Hermes Agent 教學，把 Telegram Bot、Gemini API 和基本的 Agent 功能跑起來。

---

## 🛠️ 實作過程

一開始基本上都是照著老師的教學一步一步設定。

不過實際操作後發現，現在的 Gemini API 跟老師當時做教學時有一些差異。

<font color="blue">

老師原本使用的是 `AIza...` 開頭的 API Key，但 Gemini 更新後，我這次取得的是 `AQ.` 開頭的 Key，所以原本的設定方式沒辦法完全直接套用。

</font>

---

## 🐛 遇到的問題

使用 `AQ.` Key 後，Hermes Agent 的 API routing 出現問題，不斷失敗，出現：

```text
403 BILLING_DISABLED
```

起初研判是 Billing 相關問題，但由於不希望為了測試而開啟付費功能，因此改為透過與 GPT 持續對話，逐步測試與排查，最終找出造成問題的設定。

---

## 🔧 解決方式

透過與 GPT 來回討論與測試，調整了原本的 API 設定方式。

重新測試後：

```text
Gemini API → HTTP 200
```

接著重新啟動 Gateway，Telegram 也可以正常收到 Agent 的回覆。

---

## 📱 Phase 1 測試結果

目前已完成：

* Telegram Bot
* Gemini API 串接
* Hermes Agent
* Telegram 基本對話
* 終端機工具操作

也完成老師教學中的 Phase 1 基本功能。

另外在測試工具時遇到 Gemini Free Tier 額度限制：

```text
429 RESOURCE_EXHAUSTED
```

所以先暫停測試，避免繼續消耗額度。

---

## 💡 今日心得

這次原本只是想照著教學做，但實際操作後才發現 API 已經有更新。

最大的收穫是遇到問題後，沒有只一直改設定，而是去看錯誤訊息和原始碼，最後找到 API routing 的問題並解決。

---

## 🚀 下一步

Phase 1 完成後，接下來開始做自己的 Agent：

* Custom Persona
* 個性化設定
* 回答風格
* 口頭禪
* 自訂行為規則

最後希望把它慢慢做成自己的 **AI Digital Twin**。
