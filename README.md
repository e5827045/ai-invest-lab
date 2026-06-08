# AI投資小白研究室｜商用靜態版

這是一個可直接上傳到 GitHub Pages 的內容網站 MVP。

## 包含功能
- 商業化首頁
- 文章列表與搜尋/分類
- 8 篇示範文章
- ETF 複利試算機
- AI 投資 Prompt 庫
- FAQ
- 關於、聯絡、隱私權政策
- robots.txt
- sitemap.xml
- AdSense 廣告版位預留
- 電子報區塊預留

## 上線方式
1. 解壓縮 zip
2. 將全部檔案上傳到 GitHub repository
3. 到 Settings → Pages
4. Source 選 Deploy from a branch
5. Branch 選 main / root
6. 等待 GitHub Pages 部署完成

## 修改正式資訊
上線前請修改：
- contact.html 的 Email
- legal/privacy.html 的內容
- sitemap.xml 與 robots.txt 的網站網址
- index.html 的電子報說明
- 廣告預留區改成 AdSense 程式碼

## 新增文章
1. 複製 articles/what-is-etf.html
2. 改檔名，例如 articles/new-post.html
3. 修改 title、description、h1 與內文
4. 在 assets/js/articles-data.js 新增一筆文章資料
5. 在 sitemap.xml 加入新文章網址
