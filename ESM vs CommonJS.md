# 🧠 Шпаргалка: ESM vs CommonJS

## 📦 Синтаксис

|     | ESM                         | CommonJS                    |
|-----|-----------------------------|-----------------------------|
| Импорт | `import x from 'mod'`       | `const x = require('mod')`  |
| Экспорт | `export default x`          | `module.exports = x`        |

---

## ⚡ Загрузка

- **ESM** — асинхронная загрузка (`import()`), можно загружать модули динамически
- **CommonJS** — синхронная загрузка, блокирует выполнение

---

## 🔧 Совместимость

- **ESM**: работает в браузерах и Node.js 14+
- **CommonJS**: традиционный формат Node.js

---

## 🔨 Tree shaking

- **ESM** — поддерживает, можно удалять неиспользуемый код
- **CommonJS** — не поддерживает, `require` динамический

---

## 🌀 Взаимодействие

- CommonJS → ESM: можно только через `import()` (асинхронно)
- ESM → CommonJS: можно импортировать, но только `default` экспорт

---

## 📁 Dual-package (оба формата)

```json
{
  "main": "dist/index.cjs.js",     // CommonJS
  "module": "dist/index.esm.js"    // ESM
}