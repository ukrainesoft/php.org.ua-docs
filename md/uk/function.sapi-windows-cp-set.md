---
navigation:
  - function.sapi-windows-cp-is-utf8.md: « sapi\_windows\_cp\_is\_utf8
  - function.sapi-windows-generate-ctrl-event.md: sapi\_windows\_generate\_ctrl\_event »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: sapi\_windows\_cp\_set
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sapi\_windows\_cp\_set

(PHP 7 >= 7.1.0, PHP 8)

sapi\_windows\_cp\_set — Встановити кодову сторінку процесу

### Опис

```methodsynopsis
sapi_windows_cp_set(int $codepage): bool
```

Встановити кодову сторінку поточного процесу.

### Список параметрів

`codepage`

Ідентифікатор кодової сторінки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [sapi\_windows\_cp\_get()](function.sapi-windows-cp-get.md) \- Отримати поточну кодову сторінку
