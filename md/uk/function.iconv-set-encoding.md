---
navigation:
  - function.iconv-mime-encode.md: « iconvmimeencode
  - function.iconv-strlen.md: iconvstrlen »
  - index.md: PHP Manual
  - ref.iconv.md: Функции iconv
title: iconvsetencoding
---
# iconvsetencoding

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

iconvsetencoding — Встановлює поточні налаштування для перетворення символів кодування

### Опис

```methodsynopsis
iconv_set_encoding(string $type, string $encoding): bool
```

Змінює значення вказаної параметром `type` внутрішньої змінної конфігурації на `encoding`

### Список параметрів

`type`

Значення `type` може бути одним із наведених нижче:

-   inputencoding
-   outputencoding
-   internalencoding

`encoding`

Набір символів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **iconvsetencoding()****

```php
<?php
iconv_set_encoding("internal_encoding", "UTF-8");
iconv_set_encoding("output_encoding", "ISO-8859-1");
?>
```

### Дивіться також

-   [iconvgetencoding()](function.iconv-get-encoding.md) - Отримує поточне значення налаштувань перетворення кодувань
-   [проiconvhandler()](function.ob-iconv-handler.md) - Перетворює символи з поточного кодування на кодування вихідного буфера
