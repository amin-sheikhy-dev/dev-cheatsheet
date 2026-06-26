# 🔧 ساخت اسنیپت (Snippet) در VS Code

[← بازگشت به فهرست اصلی](README.md)

اسنیپت‌ها به شما امکان می‌دهند با تایپ یک **پیشوند (prefix)**، یک بلاک کد آماده وارد کنید.

---

## 📂 مسیر ساخت اسنیپت در VS Code

1. از منوی `File` → `Preferences` → `Configure User Snippets` را انتخاب کنید.
2. گزینه `New Global Snippets file` را بزنید.
3. یک نام مثل `mysnippets` وارد کنید.
4. فایل `mysnippets.code-snippets` باز می‌شود.
5. کد JSON زیر را در آن جایگذاری کنید.

---

## 📝 مثال: فایل `mysnippets.code-snippets`

```json
{
  "console.log()": {
    "scope": "javascript,typescript,javascriptreact,typescriptreact",
    "prefix": "clg",
    "body": ["console.log($0)"]
  },
  "function () {}": {
    "scope": "javascript,typescript,javascriptreact,typescriptreact",
    "prefix": "fu",
    "body": ["function $0() {}"]
  },
  "const variable": {
    "scope": "javascript,typescript,javascriptreact,typescriptreact",
    "prefix": "co",
    "body": ["const "]
  },
  "let variable": {
    "scope": "javascript,typescript,javascriptreact,typescriptreact",
    "prefix": "le",
    "body": ["let "]
  },
  "return": {
    "scope": "javascript,typescript,javascriptreact,typescriptreact",
    "prefix": "re",
    "body": ["return "]
  },
  "require('')": {
    "scope": "javascript,typescript",
    "prefix": "req",
    "body": ["const $0 = require('$0')"]
  },
  "useState Hook": {
    "scope": "javascript,typescript,javascriptreact,typescriptreact",
    "prefix": "sta",
    "body": ["const [${1:state}, set${1/(.*)/${1:/capitalize}/}] = useState($2)"]
  },
  "useEffect Hook": {
    "scope": "javascript,typescript,javascriptreact,typescriptreact",
    "prefix": "eff",
    "body": ["useEffect(() => {$0}, [])"]
  },
  "Component": {
    "prefix": "com",
    "scope": "javascript,typescript,javascriptreact,typescriptreact",
    "body": [
      "export default function $0${TM_FILENAME_BASE/(^|[-_])(\\w)/${2:/upcase}/g}() {",
      "  return (",
      "    <div>",
      "      <p>${TM_FILENAME_BASE} Component</p>",
      "    </div>",
      "  );",
      "}"
    ]
  }
}
```
