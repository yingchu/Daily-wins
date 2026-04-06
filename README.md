# Daily-wins 小勝利記錄器
每天記錄小小的成功，讓大腦感受到成就感，養成好習慣。
Track your small daily wins. Build momentum. Feel good about yourself.
# 小勝利日記 · Daily Wins Tracker ✨

> 每天記錄小小的成功，讓大腦感受到成就感，養成好習慣。
> Track your small daily wins. Build momentum. Feel good about yourself.

[![License: MIT](https://img.shields.io/badge/License-MIT-orange.svg)](https://opensource.org/licenses/MIT)
[![Single File](https://img.shields.io/badge/size-single%20HTML%20file-brightgreen)](./小勝利日記.html)
[![No Install](https://img.shields.io/badge/install-none%20required-blue)](./小勝利日記.html)

---

## 為什麼要做這個？ / Why?

健康手環和大型 App 的習慣追蹤功能，用起來往往沒什麼成就感——通知太多、介面太複雜。
這個工具只做一件事：**讓你每天打幾個勾，然後感覺很好。**

Most habit-tracking apps feel overwhelming. Notifications. Subscriptions. Too many features.
This tool does one thing well: **let you check off your daily habits and feel great about it.**

---

## 功能 / Features

- ✅ **自訂習慣** — 加入任何你想追蹤的目標，選擇喜歡的 emoji
  Custom habits with emoji icons
- 🔥 **連續天數** — 追蹤你的連續達成紀錄，捨不得斷掉
  Streak tracking to keep your momentum going
- 📊 **本週 & 本月熱力圖** — 一眼看出哪天表現最好
  Weekly view + monthly heatmap calendar
- 🎉 **完成動畫** — 每次打勾都有小小的慶祝
  Satisfying animations when you complete a habit
- 📁 **資料存在你自己的電腦** — 使用 File System Access API，你選擇 JSON 存在哪裡
  Data stays on your device. You choose where to save your JSON file.
- 🔄 **備用匯出 / 匯入** — 所有瀏覽器都適用的備份方式
  JSON export/import fallback for all browsers
- 📱 **手機優先設計** — 在手機上也好看好用
  Mobile-first design

---

## 如何使用 / How to Use

### 最簡單的方式 / Easiest way

1. 下載 `小勝利日記.html` / Download `小勝利日記.html`
2. 雙擊開啟（建議用 Chrome 或 Edge）/ Double-click to open (Chrome or Edge recommended)
3. 選擇「全新開始」或開啟已有的資料檔 / Choose "Start Fresh" or open an existing data file
4. 開始打勾！/ Start checking off habits!

### 用 GitHub Pages 直接在瀏覽器存取 / Use GitHub Pages (no download needed)

如果 fork 這個 repo，可以開啟 GitHub Pages，直接用網址存取：
Fork this repo, enable GitHub Pages, and access it via URL — no download needed.

```
Settings → Pages → Source: Deploy from a branch → main / (root)
```

---

## 瀏覽器支援 / Browser Compatibility

| 瀏覽器 / Browser | 自動存檔 / Auto-save | 備用匯出 / JSON Export |
|:---|:---:|:---:|
| Chrome 86+       | ✅ | ✅ |
| Edge 86+         | ✅ | ✅ |
| Safari           | ❌ | ✅ |
| Firefox          | ❌ | ✅ |

> **為什麼推薦 Chrome / Edge？**
> 這兩個瀏覽器支援 [File System Access API](https://developer.mozilla.org/en-US/docs/Web/API/File_System_Access_API)，可以直接讀寫你電腦上的 JSON 檔案，不需要每次手動下載備份。

---

## 資料結構 / Data Schema

資料以 JSON 格式存在你自己電腦的任何位置，結構如下：
Data is stored as a JSON file anywhere on your computer:

```json
{
  "version": 1,
  "habits": [
    { "id": "1", "name": "晚上12點前上床", "icon": "🌙" }
  ],
  "completions": {
    "2026-04-06": ["1"]
  }
}
```

---

## 給工程師 / For Developers

這是一個**零依賴的單一 HTML 檔案**，所有 CSS 和 JavaScript 都在同一個檔案裡。
It's a **zero-dependency single HTML file** — CSS and JS all in one place.

**想要擴充？一些建議方向：**
**Want to extend it? Some ideas:**

- 🔔 **推播提醒** — 搭配 [Notifications API](https://developer.mozilla.org/en-US/docs/Web/API/Notifications_API)
  Push reminders using the Web Notifications API
- ☁️ **雲端同步** — 串接 Firebase / Supabase
  Cloud sync via Firebase or Supabase
- 🌙 **深色模式** — 修改 CSS 變數 `:root` 即可
  Dark mode by overriding `:root` CSS variables
- 🏷️ **習慣分類** — 在資料結構加入 `category` 欄位
  Habit categories by adding a `category` field to the schema
- 📤 **分享功能** — 用 Web Share API 分享當天成果
  Share daily results using the Web Share API

歡迎開 Issue 或 PR！/ Issues and PRs are welcome!

---

## 安全性 / Security

**資料隱私 / Privacy**

- 本工具完全在本地端運行，**不連線任何伺服器**，不收集任何資料。
- This tool runs entirely in your browser. **No server, no analytics, no data collection.**
- 您的習慣記錄只存在您自己選擇的 JSON 檔案裡。
- Your data lives only in the JSON file you choose on your own device.

**⚠️ 請只開啟您信任的來源提供的 JSON 資料檔**

從不明來源收到的 `.json` 資料檔，有可能包含惡意習慣名稱。雖然本工具已對所有輸入做 HTML 跳脫處理（XSS 防護），仍建議只使用自己產生的資料檔。

**⚠️ Only open JSON data files from sources you trust.**

Although this tool escapes all user-supplied content before rendering (XSS protection), you should only open data files you generated yourself or received from people you trust.

---

## 免責宣言 / Disclaimer

本工具以「現狀」提供（MIT License），**不提供任何形式的保證**。請自行備份您的資料。作者不對任何資料遺失負責。

This tool is provided "as is" under the MIT License, **without warranty of any kind**. Please back up your data regularly. The author is not responsible for any data loss.

本工具僅供個人習慣追蹤使用，**不構成任何醫療、心理健康或生活建議**。
This tool is for personal habit tracking only and **does not constitute medical, mental health, or lifestyle advice.**

---

## 授權 / License

MIT License — 自由使用、修改、發布。
Free to use, modify, and redistribute.

---

*Made with ❤️ as part of [Project Eva](https://github.com/yingchu/Daily-wins) — building small tools for a better daily life.*
