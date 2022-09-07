---
navigation:
  - function.base64-decode.md: « base64decode
  - function.get-headers.md: getheaders »
  - index.md: PHP Manual
  - ref.url.md: Функції URL
title: base64encode
---
# base64encode

(PHP 4, PHP 5, PHP 7, PHP 8)

base64encode — Кодує дані у формат MIME base64

### Опис

```methodsynopsis
base64_encode(string $string): string
```

Кодує `string` з base64.

Це кодування призначене для коректної передачі бінарних даних за протоколами, які не підтримують 8-бітну передачу, наприклад, для відправлення тіла листа.

Дані, закодовані base64, займають на 33% більше місця в порівнянні з оригінальними даними.

### Список параметрів

`string`

Дані кодування.

### Значення, що повертаються

Кодовані дані у вигляді рядка.

### Приклади

**Приклад #1 Приклад використання **base64encode()****

```php
<?php
$str = 'Это закодированная строка';
echo base64_encode($str);
?>
```

Результат виконання цього прикладу:

```
0K3RgtC+INC30LDQutC+0LTQuNGA0L7QstCw0L3QvdCw0Y8g0YHRgtGA0L7QutCw
```

### Дивіться також

-   [base64decode()](function.base64-decode.md) - Декодує дані, закодовані MIME base64
-   [chunksplit()](function.chunk-split.md) - Розбиває рядок на фрагменти
-   [convertuuencode()](function.convert-uuencode.md) - Кодує рядок у форматі uuencode
-   [» RFC 2045](http://www.faqs.org/rfcs/rfc2045) розділ 6.8
