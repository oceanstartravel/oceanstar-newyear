# 2027 春節旅遊專頁｜維護說明

## 檔案用途

- `index.html`：網站文字內容、Logo、圖片網址、行程標題與連結、SEO 標題／描述。
- `style.css`：所有視覺樣式，例如底色、字體、間距、桌機與手機版排版。
- `MAINTENANCE.md`：給接手同事看的簡易維護說明。

## 常見修改位置

在 `index.html` 使用 Ctrl+F 搜尋以下註解：

- `[區塊 1]`：頁首 Logo 與「2027 春節旅遊精選」標題與旅遊諮詢／LINE 客服按鈕。
- `[區塊 2]`：春節主視覺圖片與點擊後前往的網址。
- `[區塊 3]`：專題介紹與國家快速選單。
- `[區塊 4]`：國家分類與行程卡片。
- `[區塊 5]`：行程內容下方的旅遊諮詢、LINE 客服與 Facebook 入口。
- `[區塊 6]`：官網風格頁尾與公司資訊。
- `.floating-contact`：桌機與手機都會固定顯示的三個聯絡按鈕。
- `.back-to-top`：右下角藍色 TOP 浮標使用 CSS 繪製屋頂形向上尖角（不使用文字 ↑ 符號）。

## 修改底色、字體、間距

請開啟 `style.css`，使用 Ctrl+F 搜尋 CSS 類別名稱，例如：

- `.site-header`：頁首整條 BAR 的底色與邊框。
- `.header-topic`：頁首「2027 春節旅遊精選」標題與旅遊諮詢／LINE 客服按鈕樣式。
- `.hero`、`.hero img`：主視覺區域與圖片顯示方式。
- `.intro`：主視覺下方的專題介紹區塊。
- `.quick-nav`：國家快速選單。
- `.country-heading`：國家標題色帶。
- `.trip-card`：行程卡片外觀。
- `@media`：手機版與較小螢幕的版面規則。

## 聯絡入口

頁首與頁尾的「旅遊諮詢」連結為 `https://www.oceanstar.com.tw/query.html`；「LINE 客服」連結為 `https://page.line.me/tje7738k?openQrModal=true`。頁面底部固定顯示三個聯絡入口：旅遊諮詢、LINE 客服與 Facebook 粉絲專頁。

## 新增或修改行程

1. 在 `index.html` 搜尋 `[區塊 4]`。
2. 找到對應國家，再複製該國家底下既有的 `<article class="trip-card"> ... </article>`。
3. 修改行程標題、說明文字與正式官網連結。
4. 確認連結能開啟正確行程頁，再提交變更。

## 新增國家選單時

快速選單的 `href="#vietnam"` 必須與內容區塊的 `id="vietnam"` 完全一致。新增選單時，也要新增相同 ID 的內容區塊；否則選單會跳不到正確位置。

## 頁尾與固定聯絡列

- 頁尾只保留深灰色公司資料區，不再顯示「特別報導／旅遊資訊／文件與服務／相關連結」四欄區塊。
- 固定聯絡列的 Facebook 連結為 `https://www.facebook.com/oceanstar16774819/`，直接前往新粉絲專頁，不使用 Messenger 管理或登入網址。
- 右下角藍色 TOP 浮標使用 CSS 繪製屋頂形向上尖角（不使用文字 ↑ 符號）位於固定聯絡列上方，點擊可回到頁首。

## 發布方式

GitHub 專案根目錄至少要同時有：
- `index.html`
- `style.css`

修改後提交到 `main` 分支，等待 GitHub Pages 部署，再重新整理網站檢查。若只更新 `index.html`、忘記更新 `style.css`，新樣式就不會生效。
