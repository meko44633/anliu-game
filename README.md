# 暗流 — GitHub Pages 手機網站版

已整理成可直接部署的靜態網站，不需付費 API、伺服器、資料庫。

## 你需要做的事（GitHub 帳戶持有人）

1. 在 https://github.com/new 建立一個 **Public** repository，建議名稱為 `anliu-game`，分支用 `main`。
2. 在新 repository 選 **Add file → Upload files**，**將本 ZIP 解壓後的所有檔案**（包含 `index.html`、`sw.js`、`manifest.webmanifest`、圖示）上傳到 repository 根目錄。注意不要把上層資料夾也一起上傳。
3. 按 **Commit changes**。
4. 進入 **Settings → Pages**；在 **Build and deployment** 裏面將 **Source** 設定為 **Deploy from a branch**、**Branch** 選 `main`、**Folder** 選 `/(root)`，按 **Save**。
5. 待部署狀態顯示成功後，網頁通常位於 `https://你的GitHub用戶名稱.github.io/anliu-game/`。以 GitHub Pages 顯示的確實網址為準。
6. iPhone 使用 Safari 打開網站 → 分享按鈕 → **加入主畫面**。之後就像 App 一樣開啟。

> 注意：GitHub Free 的 GitHub Pages 需要 Public repository。此遊戲程式與內建虛構案件將公開，但玩家實際玩的進度只保留在自己的裝置瀏覽器中（localStorage），不會上傳到 GitHub。請不要在 Repository 放私人資訊。

## 檔案
- `index.html`：完整遊戲
- `manifest.webmanifest`：手機主畫面資訊
- `sw.js`：首次在線載入後可支援離線使用
- `icon-192.png`、`icon-512.png`、`apple-touch-icon.png`：手機圖示
- `.nojekyll`：避免被 Jekyll 處理

## 更新
以新版本檔案替換 repository 根目錄相同檔名即可。若更改離線網站資源，亦應更新 `sw.js` 內的 `CACHE_NAME` 版本字串。
