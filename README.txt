SimTrade 獨立 PWA（已移除 Claude 帳號同步）

檔案：
- index.html：遊戲本體
- manifest.json：PWA 安裝資訊
- sw.js：離線快取
- icons/：應用程式圖示

已移除：
- Claude 使用者／資料庫 API 讀取
- Claude 雲端存檔同步
- Claude 下載 API

保留：
- localStorage 本機自動存檔
- 匯出／匯入存檔碼
- 瀏覽器原生存檔檔案下載

發布方式：
1. 將 ZIP 解壓縮。
2. 把裡面的 index.html、manifest.json、sw.js、icons 資料夾上傳到 GitHub repository 根目錄。
3. 在 GitHub repository 的 Settings → Pages 啟用部署。
4. 用 GitHub Pages 的 HTTPS 網址在 Android Chrome 開啟。
5. Chrome 選單中找「安裝應用程式」或「加入主畫面」（選項名稱依版本而異）。

重要：
- 不要直接從手機檔案管理器開啟 index.html 期待 PWA 安裝；請用 HTTPS 網址。
- localStorage 是依網站來源分開保存的。原本 file:// 或 Claude 環境裡的存檔不會自動搬到 GitHub Pages；發布前請先在舊版本匯出存檔碼，之後再在新網站匯入。
- 這份 ZIP 移除了 Claude 同步依賴，但仍請先自行測試遊戲、存檔匯出／匯入和離線啟動。
