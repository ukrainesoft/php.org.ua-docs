---
navigation:
  - function.php-strip-whitespace.md: « php\_strip\_whitespace
  - function.sapi-windows-cp-get.md: sapi\_windows\_cp\_get »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: sapi\_windows\_cp\_conv
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sapi\_windows\_cp\_conv

(PHP 7 >= 7.1.0, PHP 8)

sapi\_windows\_cp\_conv — Перетворює рядок із однієї кодової сторінки на іншу

### Опис

```methodsynopsis
sapi_windows_cp_conv(int|string $in_codepage, int|string $out_codepage, string $subject): ?string
```

Перетворює рядок з однієї кодової сторінки на іншу.

### Список параметрів

`in_codepage`

Кодова сторінка рядка `subject`. Або ім'я чи ідентифікатор кодової сторінки.

`out_codepage`

Кодовая страница для преобразования строки`subject`. Або ім'я чи ідентифікатор кодової сторінки.

`subject`

Рядок для перетворення.

### Значення, що повертаються

Рядок `subject`, перетворена на кодову сторінку `out_codepage`или\*\*`null`\*\*в случае возникновения ошибки.

### Помилки

Ця функція видасть помилки рівня E\_WARNING, якщо передані неприпустимі кодові сторінки, або якщо рядок у параметрі subject некоректний для кодової сторінки `in_codepage`

### Дивіться також

-   [sapi\_windows\_cp\_get()](function.sapi-windows-cp-get.md) \- Отримати поточну кодову сторінку
-   [iconv()](function.iconv.md) \- Перетворює рядок з одного кодування символів на інший
