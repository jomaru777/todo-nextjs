# Next.js Todo App

────────────────────────────────────────
(日本語)

React + TypeScript で作成した Todoアプリ(https://github.com/jomaru777/todo-react.git)を、Next.jsで再実装したプロジェクトです。
Next.js特有の仕組み（Server / Client Components、Hydration など）を理解することを目的としています。

## リポジトリ
https://github.com/jomaru777/todo-nextjs.git

## 機能
- シンプルな Todo 管理アプリ
- 追加 / 削除 / 完了切り替えが可能
- localStorage を使ったデータ永続化

## 使用技術
- Next.js(App Router)
- React
- TypeScript

## フォルダ構成（src 配下）
app/
├─ layout.tsx        # 全体レイアウト
├─ page.tsx          # トップページ
├─ globals.css

components/
├─ todo/
│  ├─ TodoInput.tsx
│  ├─ TodoItem.tsx
│  └─ TodoList.tsx
└─ ui/
   └─ Button.tsx

hooks/
└─ useTodos.ts

types/
└─ todo.ts

## 設計・工夫した点
- Todo の状態管理とロジックをカスタムフック（useTodos）に集約
- UI コンポーネントとロジックを分離
- 共通の型定義を types/ ディレクトリに切り出し

## 学んだこと
- App Router の基本構造（layout.tsx / page.tsx）
- Server Components と Client Components の違い
- `"use client"` が必要なケース
- Hydration（サーバー描画とクライアント描画の一致）の概念

※ 現在、localStorage を使用しているため、Hydration warning が発生します。
  これは、Next.js の挙動を理解することを目的として、意図的にそのままにしています。

## 今後の改善予定
- Hydration warning の解消
- metadata の適切な設定
- コンポーネント設計の見直し

────────────────────────────────────────
## English

This project is a Next.js reimplementation of a Todo application(https://github.com/jomaru777/todo-react.git) originally built with React and TypeScript.
The goal is to understand Next.js-specific concepts such as Server / Client Components and hydration.

## repository
https://github.com/jomaru777/todo-nextjs.git

## Features
- Simple Todo management application
- Add, delete, and toggle todos
- Persistent storage using localStorage

## Tech Stack
- Next.js(App Router)
- React
- TypeScript

## Folder Structure
app/
- layout.tsx
- page.tsx
- globals.css

components/
- todo/
- ui/

hooks/
- useTodos.ts

types/
- todo.ts

## Architecture & Design
- Todo state and logic are encapsulated in a custom hook (useTodos)
- Clear separation between UI components and logic
- Shared types are defined in a dedicated types directory

## What I Learned
- App Router fundamentals
- Differences between Server and Client Components
- When and why `"use client"` is required
- The concept of hydration and hydration warnings

※ A hydration warning currently occurs due to the use of localStorage.
This is intentional to focus on understanding Next.js behavior.

## Next Steps
- Resolve hydration warnings properly
- Improve metadata and accessibility
- Refine component architecture
