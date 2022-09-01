---
navigation:
  - function.sapi-windows-cp-conv.html: « sapiwindowsспconv
  - function.sapi-windows-cp-is-utf8.html: sapiwindowsспісutf8 »
  - index.html: PHP Manual
  - ref.misc.html: Різні функції
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

-   [sapiwindowsспset()](function.sapi-windows-cp-set.html) - Встановити кодову сторінку процесу
