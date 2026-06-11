---
name: designer-survival-guide
description: >
  產出適合投影簡報與現場講解的互動式 HTML 單頁簡報工具。
  主題：設計師接需求生存術。11 個投影頁面，涵蓋需求訪談、改稿管理、報價話術、合作確認書。
  含 GA4 埋碼、SEO meta tags、互動 Checklist、話術複製、彈窗報告產生器。
  觸發關鍵字：生存指南、設計師需求、客戶需求、改稿、接案頁面、接案流程、互動網頁、HTML 簡報
---

# 設計師接需求生存術 SKILL

## 定位

此工具定位為「設計師接案流程互動簡報工具」，整合：

- 教學內容（投影簡報格式）
- 需求訪談 Checklist（互動勾選 + 對焦報告）
- 合作確認書（表單填寫 + 彈窗輸出）
- 現場互動操作（複製話術、流程圖）

讓設計師能從模糊需求走向正式合作，可投影展示也可實際操作使用。

---

## 觸發關鍵字

- 生存指南
- 設計師需求
- 客戶需求
- 改稿
- 接案頁面
- 接案流程
- 互動網頁
- HTML 簡報

---

## 輸出規格

| 項目 | 說明 |
|------|------|
| 檔名 | `designer-survival-guide.html` |
| 技術棧 | 純 HTML + CSS + Vanilla JS（零依賴） |
| 視覺風格 | Geniestudio AI SaaS 風格（黑白高對比 + 螢光綠重點色 + 格線背景） |
| SEO | title、description、keywords、robots、OG tags |
| GA4 | 預留 G-XXXXXXXXXX，含 3 個自訂事件 |
| RWD | Desktop / Tablet / Mobile（CSS clamp + flexbox + grid） |

---

## 簡報頁面結構（11 頁）

| # | 頁面 | 核心訊息 / 功能 |
|---|------|----------------|
| 1 | 開場 | 設計師接需求生存術 |
| 2 | 爆炸場景 | 設計不是從畫面開始，而是從邊界開始 |
| 3 | 需求模糊 | 先確認目標，不先問喜好 |
| 4 | 收斂技巧 | 把開放題變成選擇題 |
| 5 | 需求訪談 Checklist | 互動勾選 6 項 + 即時完成度 + 產生對焦報告彈窗 |
| 6 | 開場話術模板 | 可複製按鈕（script_id: opening） |
| 7 | 無限改稿風險 | 修改 ≠ 重做，建立修改邊界 |
| 8 | 改稿流程圖 | 需求確認 → 第一版 → 修改回饋 → 第二版 → 定稿 |
| 9 | 加價話術 | 可複製按鈕（script_id: pricing） |
| 10 | 正式合作確認 | 表單（5 欄位 + 2 checkbox）+ 產生合作確認書彈窗 |
| 11 | 總結 | 專業不是無限配合，而是讓合作變清楚 |

---

## 互動功能說明

### 頁 5 — 需求訪談 Checklist

勾選項目：

1. 確認設計最終目標
2. 確認主要使用者
3. 取得至少 3 個視覺參考
4. 確認不要的方向
5. 確認交付格式與時程
6. 需求確認書已取得書面確認

功能：
- 即時顯示完成度（如 3/6）
- 點擊「產生對焦報告」按鈕後彈窗顯示：
  - 需求清晰度評估
  - 已完成項目列表
  - 尚需補齊項目列表
  - 下一步建議

### 頁 6 / 頁 9 — 話術複製

- 點擊複製按鈕 → 複製文字到剪貼簿
- 觸發 GA4 `copy_script` 事件

### 頁 10 — 正式合作確認

表單欄位：
- 委託方名稱
- 專案名稱
- 預計時程
- 修改輪數
- 備註

Checkbox：
- 已確認交付範圍
- 已同意合作條款

功能：
- 點擊「產生合作確認書」→ 彈窗顯示整理後的合作確認摘要

---

## 視覺設計規範

| 項目 | 規格 |
|------|------|
| 主色 | 黑 `#0a0a0a` |
| 背景 | 深灰 `#111` + 細格線紋理 |
| 重點色 | 螢光綠 `#b8f53c` |
| 文字 | 白 `#ffffff` / 淺灰 `#888` |
| 標題字級 | clamp(2.5rem, 8vw, 6rem) |
| 卡片 | 圓角 16px + 輕量陰影 + border `#222` |
| 版型 | 一屏一重點，低資訊密度 |
| 避免 | 花俏動畫、過度裝飾、吉祥物、小字排版 |

---

## GA4 事件規格

| 事件名稱 | 觸發時機 | 參數 |
|----------|----------|------|
| `tab_switch` | 切換場景 Tab | `{ tab_name: "fog" \| "loop" }` |
| `checklist_item` | 勾選/取消 checklist | `{ item_id: "...", checked: true\|false }` |
| `copy_script` | 點擊複製話術按鈕 | `{ script_id: "opening" \| "pricing" }` |

---

## SEO Head 規格

```html
<title>設計師接需求生存術｜職人互動生存指南</title>
<meta name="description" content="設計師接案流程互動指南，涵蓋需求訪談、改稿管理、報價與合作確認。">
<meta name="keywords" content="設計師,接案,需求訪談,改稿,報價,合作流程">
<meta name="robots" content="index,follow">
<meta property="og:title" content="設計師接需求生存術｜職人互動生存指南">
<meta property="og:description" content="設計師接案流程互動指南，涵蓋需求訪談、改稿管理、報價與合作確認。">
<meta property="og:type" content="website">
<meta property="og:image" content="og-cover.png">
```

---

## 互動規則

互動元件（input、textarea、select、checkbox、button）取得焦點時，**禁止左右方向鍵切頁**，避免干擾簡報操作。

---

## 部署方式（GitHub Pages）

```
1. 將 designer-survival-guide.html 重新命名為 index.html
2. 上傳至 GitHub repo（設為 Public）
3. Settings → Pages → Deploy from branch (main)
4. 取得網址：https://你的帳號.github.io/repo名稱/
```

替換 GA4 ID：

```bash
sed -i 's/G-XXXXXXXXXX/G-你的真實ID/g' index.html
```

---

## 延伸開發建議

- 新增「報價談判術」頁面
- LocalStorage 保存 Checklist 狀態
- Google Form 整合提交案例
- PDF 匯出合作確認書
- Notion API 整合
- CRM 串接

---

## 檔案清單

```
designer-survival-guide/
├── SKILL.md                       ← 本說明文件
└── designer-survival-guide.html  ← 主網頁（投影簡報 + 互動工具）
```
