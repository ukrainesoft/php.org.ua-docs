---
navigation:
  - function.iconv-mime-encode.md: « iconv\_mime\_encode
  - function.iconv-strlen.md: iconv\_strlen »
  - index.md: PHP Manual
  - ref.iconv.md: Функції iconv
title: iconv\_set\_encoding
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# iconv\_set\_encoding

(PHP 4 >= 4.0.5, PHP 5, PHP 7, PHP 8)

iconv\_set\_encoding — Встановлює поточні налаштування для перетворення символів кодування

### Опис

```methodsynopsis
iconv_set_encoding(string $type, string $encoding): bool
```

Змінює значення вказаної параметром `type` внутрішньої змінної конфігурації на `encoding`

### Список параметрів

`type`

Значение`type` може бути одним із наведених нижче:

-   input\_encoding
-   output\_encoding
-   internal\_encoding

`encoding`

Набір символів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** iconv\_set\_encoding()\*\*\*\*

```php
<?php
iconv_set_encoding("internal_encoding", "UTF-8");
iconv_set_encoding("output_encoding", "ISO-8859-1");
?>
```

### Дивіться також

-   [iconv\_get\_encoding()](function.iconv-get-encoding.md) \- Отримує поточне значення налаштувань перетворення кодувань
-   [ob\_iconv\_handler()](function.ob-iconv-handler.md) \- Перетворює символи з поточного кодування на кодування вихідного буфера
