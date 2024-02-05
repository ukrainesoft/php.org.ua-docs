---
navigation:
  - function.sapi-windows-cp-conv.md: « sapi\_windows\_cp\_conv
  - function.sapi-windows-cp-is-utf8.md: sapi\_windows\_cp\_is\_utf8 »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: sapi\_windows\_cp\_get
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sapi\_windows\_cp\_get

(PHP 7 >= 7.1.0, PHP 8)

sapi\_windows\_cp\_get — Отримати поточну сторінку.

### Опис

```methodsynopsis
sapi_windows_cp_get(string $kind = ""): int
```

Отримати поточну сторінку.

### Список параметрів

`kind`

Тип кодової сторінки операційної системи, яку потрібно отримати: або `'ansi'`, либо`'oem'`. Будь-яке інше значення стосується поточної кодової сторінки процесу.

### Значення, що повертаються

Якщо `kind`равен`'ansi'`повертається поточна кодова сторінка ANSI операційної системи. Якщо `kind`равен`'oem'`, повертається поточна кодова сторінка OEM операційної системи. В іншому випадку поточна кодова сторінка процесу повертається.

### Дивіться також

-   [sapi\_windows\_cp\_set()](function.sapi-windows-cp-set.md) \- Встановити кодову сторінку процесу
