# E-commerce Landing

一個可直接使用 Node.js + Vite 執行的電商 Landing Page 範例。

## 專案結構

- `index.html`：Landing Page
- `data/products.json`：共用假資料，商品、Hero、Feature、Footer 資料都集中在這裡
- `js/app.js`：讀取 JSON 並產生畫面
- `scss/_variables.scss`：共用 SCSS 變數
- `scss/_header.scss`：Header
- `scss/_product.scss`：商品區與商品 Card
- `scss/_landing.scss`：Base、Hero、Feature
- `scss/_footer.scss`：Footer
- `scss/all.scss`：SCSS 統一入口
- `images/`：範例圖片（SVG，可直接替換）
- `css/all.css`：Vite build 後產生

## 安裝

```bash
npm install
```

## 開發

```bash
npm run dev
```

開啟終端機顯示的 localhost 網址即可。

## 建置

```bash
npm run build
```

Vite 會產生 `dist/`。

## 修改假資料

主要修改：

```text
data/products.json
```

例如：

```json
{
  "name": "新的商品名稱",
  "price": 999,
  "originalPrice": 1299,
  "image": "/images/my-product.svg",
  "tag": "新品"
}
```

圖片只需要放在 `images/`，再修改 JSON 的 `image` 路徑。

## SCSS

所有 SCSS 都由：

```text
scss/all.scss
```

統一 import：

```scss
@import "variables";
@import "header";
@import "product";
@import "landing";
@import "footer";
```

Vite 會處理 SCSS 並輸出 CSS。
