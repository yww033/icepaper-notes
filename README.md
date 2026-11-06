# 論文研讀批注

學術論文的雙欄批注頁面：左欄是原文和五色高亮，右欄是逐段論證分析。

網站網址：https://yww033.github.io/icepaper-notes/

GitHub repo：https://github.com/yww033/icepaper-notes

## 資料夾結構

```
paper-notes/
├── index.html      ← 首頁（論文清單）
├── papers/         ← 每篇論文一個 .html
│   └── 2022-auto-feature-dataset-shift.html
├── .nojekyll       ← 讓 GitHub Pages 直接提供檔案，不經過 Jekyll 處理
└── README.md
```

## 新增一篇論文

1. 把批注 HTML 複製進 `papers/`，改成英文檔名，格式是 `年份-英文關鍵字.html`，例如 `2023-credit-risk-gnn.html`。
2. 在論文頁的 `<div class="kicker">` 前面，加上回首頁的連結：
   `<a class="home" href="../index.html">← 回論文批注首頁</a>`
3. 打開 `index.html`，在 `PAPERS` 陣列最前面複製一個 `{ ... }` 區塊，把 `file`、`title`、`summary`、`tags`、`added` 等欄位改成新論文的資料。
4. 上傳：
   ```bash
   git add .
   git commit -m "新增論文：<論文簡稱>"
   git push
   ```
   等 1～2 分鐘，網站就會更新。

## 版本管理

網站裡的檔名必須固定，網址才不會失效，所以這裡不用 `_v2`、`_v3` 的命名。每次修改的歷史都記錄在 git 裡，可以用 `git log` 查看。工作中的各個版本，則保留在原本的研究資料夾。
