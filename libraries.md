# کتابخانه‌ها و راه‌اندازی پروژه

[← بازگشت به فهرست اصلی](README.md)

## ساخت پروژه با Vite

```bash
npm create vite@latest
npm i
npm run dev
```

---

## ساخت پروژه با Next.js

```bash
npx create-next-app@latest
npm run dev
```

### برای Build گرفتن

```bash
npm run build
npm start
```

### در `Next.js 15` به بعد اگه اگه مشکل مصرف cpu و ram داشتید فلگ `--webpack` را داخل `package.json` اضافه کنید

```json
"scripts": {
  "dev": "next dev --webpack",
  "build": "next build",
  "start": "next start",
  "lint": "eslint"
}
```

---

## نصب Tailwind CSS 3

```bash
npm i -D tailwindcss@3 postcss autoprefixer
npx tailwind init -p
```

فایل‌های زیر باید ساخته شوند:

- tailwind.config.js
- postcss.config.js

## تنظیم tailwind.config.js

```js
/** @type {import('tailwindcss').Config} */
export default {
  darkMode: 'class', // برای دارک مود ضروریه
  content: ['./src/**/*.{html,js,jsx,ts,tsx}', './public/index.html'],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

## تنظیم global.css یا index.css

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

## Dark Mode

```css
@layer base {
  body {
    @apply bg-white dark:bg-gray-900;
  }
}
```

## مرتب‌ سازی کلاس‌ های Tailwind

```bash
npm i -D prettier prettier-plugin-tailwindcss
```

ابتدا ساخت یک فایل
`.prettierrc`
و قرار دادن متن زیر داخلش

```json
{
  "plugins": ["prettier-plugin-tailwindcss"],
  "printWidth": 150,
  "singleQuote": true,
  "jsxSingleQuote": true,
  "tsxSingleQuote": true,
  "semi": true,
  "trailingComma": "es5",
  "bracketSpacing": true,
  "tabWidth": 2,
  "useTabs": false,
  "arrowParens": "always",
  "htmlWhitespaceSensitivity": "ignore"
}
```

---

# کتابخانه‌ها

## React Router

```bash
npm i react-router-dom
```

## Redux Toolkit

```bash
npm i @reduxjs/toolkit
npm i react-redux
```

## Zustand

```bash
npm i zustand
```

## React Query

```bash
npm i @tanstack/react-query
```

## React Icons

```bash
npm i react-icons
```

## Framer Motion

```bash
npm i framer-motion
```

## Swiper

```bash
npm i swiper
```

## Supabase

```bash
npm i @supabase/supabase-js
```

## SQLite

```bash
npm i better-sqlite3
```

## Backend & Security

```bash
npm i slugify xss
```

## Next Themes

```bash
npm i next-themes
```

## Next Client Cookies

```bash
npm i next-client-cookies
```

## Next Intl

```bash
npm i next-intl
```

## Jalali Date

```bash
npm i date-fns-jalali
```

## TypeScript (Global)

```bash
npm i -g typescript
```
