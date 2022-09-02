---
navigation:
  - function.sapi-windows-cp-conv.md: « sapiwindowsспconv
  - function.sapi-windows-cp-is-utf8.md: sapiwindowsспісutf8 »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: sapiwindowsспget
---
# sapiwindowsспget

(PHP 7> = 7.1.0, PHP 8)

sapiwindowsспget — Отримати поточну сторінку.

### Опис

```methodsynopsis
sapi_windows_cp_get(string $kind = ""): int
```

Отримати поточну сторінку.

### Список параметрів

`kind`

Тип кодової сторінки операційної системи, яку потрібно отримати: або `'ansi'`, або `'oem'`. Будь-яке інше значення стосується поточної кодової сторінки процесу.

### Значення, що повертаються

Якщо `kind` дорівнює `'ansi'`повертається поточна кодова сторінка ANSI операційної системи. Якщо `kind` дорівнює `'oem'`, повертається поточна кодова сторінка OEM операційної системи. В іншому випадку поточна кодова сторінка процесу повертається.

### Дивіться також

-   [sapiwindowsспset()](function.sapi-windows-cp-set.md) - Встановити кодову сторінку процесу
