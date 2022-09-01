---
navigation:
  - function.php-strip-whitespace.html: « phpstripwhitespace
  - function.sapi-windows-cp-get.html: sapiwindowsспget »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: sapiwindowsспconv
---
# sapiwindowsспconv

(PHP 7> = 7.1.0, PHP 8)

sapiwindowsспconv — Перетворити рядок з однієї кодової сторінки на іншу

### Опис

```methodsynopsis
sapi_windows_cp_conv(int|string $in_codepage, int|string $out_codepage, string $subject): ?string
```

Перетворити рядок із однієї кодової сторінки на іншу.

### Список параметрів

`in_codepage`

Кодова сторінка рядка `subject`. Або ім'я чи ідентифікатор кодової сторінки.

`out_codepage`

Кодова сторінка для перетворення рядка `subject`. Або ім'я чи ідентифікатор кодової сторінки.

`subject`

Рядок для перетворення.

### Значення, що повертаються

Рядок `subject`, перетворена на `out_codepage` або **`null`** у разі виникнення помилки.

### Помилки

Ця функція видасть помилки рівня EWARNING, якщо передані неприпустимі кодові сторінки, або якщо рядок у параметрі subject некоректний для `in_codepage`

### Дивіться також

-   [sapiwindowsспget()](function.sapi-windows-cp-get.html) - Отримати поточну кодову сторінку
-   [iconv()](function.iconv.md) - Перетворює рядок з одного кодування символів на інший
