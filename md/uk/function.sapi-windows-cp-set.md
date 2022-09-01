---
navigation:
  - function.sapi-windows-cp-is-utf8.html: « sapiwindowsспісutf8
  - function.sapi-windows-generate-ctrl-event.html: sapiwindowsgeneratectrlevent »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: sapiwindowsспset
---
# sapiwindowsспset

(PHP 7> = 7.1.0, PHP 8)

sapiwindowsспset — Встановити кодову сторінку процесу

### Опис

```methodsynopsis
sapi_windows_cp_set(int $codepage): bool
```

Встановити кодову сторінку поточного процесу.

### Список параметрів

`codepage`

Ідентифікатор кодової сторінки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [sapiwindowsспget()](function.sapi-windows-cp-get.md) - Отримати поточну кодову сторінку
