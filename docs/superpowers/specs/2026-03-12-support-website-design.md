# Miranote サポートウェブサイト — Design Document

## Overview

Miranote（ゲーム組織）のアプリサポート情報を提供するウェブサイト。App Storeのプロダクトページに表示するサポートURL用。今後複数アプリが追加される想定のため、特定アプリのテーマに依存しないニュートラルなデザイン。

## Requirements

- App Store審査に必要な最低限のサポート情報（お問い合わせメールアドレス）を掲載
- シンプル・ミニマルな構成
- レスポンシブ対応（モバイルでも見やすい）
- Vercelでデプロイ

## Architecture

### 技術構成

- 単一の `index.html`（インラインCSS）
- フレームワーク不要、ビルド不要
- 静的サイトとしてVercelにデプロイ

### ページ構成

```
┌─────────────────────────┐
│  Header: "Miranote"     │
├─────────────────────────┤
│                         │
│  Support / お問い合わせ  │
│                         │
│  メールアドレス          │
│  (mailto: リンク)       │
│                         │
├─────────────────────────┤
│  Footer: © 2026 Miranote│
└─────────────────────────┘
```

### ビジュアルデザイン

- 白背景ベースのクリーンなミニマルデザイン
- ニュートラルな配色（特定アプリに依存しない）
- レスポンシブ対応（viewport meta + flexbox）

### コンテンツ

- 組織名: Miranote
- サポートメール: th1khse@gmail.com
- 対象アプリ: NumberFusion（初期）、今後追加予定

## Deployment

- Vercel CLIまたはGitHub連携でデプロイ
- カスタムドメインなし（Vercel提供のURLを使用）

## File Structure

```
Miranote/
├── index.html
└── docs/
    └── superpowers/
        └── specs/
            └── 2026-03-12-support-website-design.md
```
