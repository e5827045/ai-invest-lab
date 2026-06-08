# AI投資小白研究室 V3

## 如何新增文章
1. 複製 `articles/etf-beginner.html`
2. 改檔名，例如 `articles/my-new-article.html`
3. 修改 `<title>`、`<h1>`、文章內容
4. 打開 `assets/js/articles-data.js`
5. 新增一筆文章資料：
```js
{
  title: "你的文章標題",
  category: "ETF",
  description: "文章簡短介紹",
  url: "articles/my-new-article.html"
}
```
6. 上傳到 GitHub，等待 GitHub Pages 重新部署。

## 目前架構
- 前端：HTML / CSS / JavaScript
- 後端：目前無後端，適合 GitHub Pages
- 未來可升級：Node.js + Express + MongoDB / PostgreSQL
