# Miranote Support Website Implementation Plan

> **For agentic workers:** REQUIRED: Use superpowers:subagent-driven-development (if subagents available) or superpowers:executing-plans to implement this plan. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Miranoteのアプリサポート情報ページを作成し、Vercelにデプロイする

**Architecture:** 単一の `index.html`（インラインCSS）による静的サイト。ビルド不要。

**Tech Stack:** HTML, CSS, Vercel CLI (`npx vercel`)

---

## Chunk 1: Implementation & Deploy

### Task 1: Create index.html

**Files:**
- Create: `index.html`

- [ ] **Step 1: Create the HTML file**

```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Miranote - Support</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
      color: #333;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }
    header {
      padding: 2rem;
      text-align: center;
      border-bottom: 1px solid #eee;
    }
    header h1 { font-size: 1.5rem; font-weight: 600; }
    main {
      flex: 1;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 3rem 1.5rem;
      text-align: center;
    }
    main h2 { font-size: 1.25rem; margin-bottom: 1rem; }
    main p { margin-bottom: 0.5rem; color: #666; }
    main a { color: #007aff; text-decoration: none; }
    main a:hover { text-decoration: underline; }
    footer {
      padding: 1.5rem;
      text-align: center;
      color: #999;
      font-size: 0.85rem;
      border-top: 1px solid #eee;
    }
  </style>
</head>
<body>
  <header>
    <h1>Miranote</h1>
  </header>
  <main>
    <h2>Support</h2>
    <p>お問い合わせは下記メールアドレスまでご連絡ください。</p>
    <p><a href="mailto:th1khse@gmail.com">th1khse@gmail.com</a></p>
  </main>
  <footer>
    <p>&copy; 2026 Miranote</p>
  </footer>
</body>
</html>
```

- [ ] **Step 2: ブラウザでローカル確認**

Run: `open index.html`（macOS）
Expected: ブラウザでページが表示され、メールリンクが機能する

- [ ] **Step 3: Git初期化とコミット**

```bash
git init
git add index.html
git commit -m "feat: add support page for App Store"
```

### Task 2: Vercelにデプロイ

- [ ] **Step 4: Vercelにデプロイ**

```bash
npx vercel --yes
```

Expected: デプロイ成功、URLが表示される

- [ ] **Step 5: デプロイされたURLをブラウザで確認**

Expected: 本番環境でページが正しく表示される

- [ ] **Step 6: 本番デプロイ**

```bash
npx vercel --prod --yes
```

Expected: 本番URLが表示される。このURLをApp StoreのサポートURLとして使用する。
