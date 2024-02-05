---
navigation:
  - function.fdf-errno.md: « fdf\_errno
  - function.fdf-get-ap.md: fdf\_get\_ap »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_error
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_error

(PHP 4 >= 4.3.0, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_error — Повертає опис помилки для коду помилки FDF

### Опис

```methodsynopsis
fdf_error(int $error_code = -1): string
```

Отримує текстовий опис коду помилки FDF, вказаного в `error_code`

### Список параметрів

`error_code`

Код помилки, отриманий за допомогою [fdf\_errno()](function.fdf-errno.md). Якщо не вказано, функція використовує код внутрішньої помилки, встановлений останньою операцією.

### Значення, що повертаються

Повертає повідомлення про помилку у вигляді рядка або рядка `no error`якщо помилки немає.

### Дивіться також

-   [fdf\_errno()](function.fdf-errno.md) \- Повертає код помилки для останньої операції FDF
