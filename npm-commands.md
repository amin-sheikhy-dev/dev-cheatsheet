# دستورات npm

[← بازگشت به فهرست اصلی](README.md)

## تغییر Registry

```bash
npm config set registry https://mirror-npm.runflare.com
```

```bash
npm config set registry https://mirror2.chabokan.net/npm/
```

```bash
npm config set registry https://package-mirror.liara.ir/repository/npm/
```

## بازگرداندن Registry پیش‌ فرض

```bash
npm config set registry https://registry.npmjs.org/
```

## مشاهده Registry فعلی

```bash
npm config get registry
```

## تست اتصال npm

```bash
npm ping
```

## بررسی نصب بودن یک پکیج

```bash
npm list packageName
```

## مشاهده نسخه npm

```bash
npm --version
```

## مشاهده نسخه Node.js

```bash
node --version
```

## توقف اجرای دستور

```text
Ctrl + C
```
