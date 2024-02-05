---
navigation:
  - function.base64-decode.md: « base64\_decode
  - function.get-headers.md: get\_headers »
  - index.md: PHP Manual
  - ref.url.md: Функції URL
title: base64\_encode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# base64\_encode

(PHP 4, PHP 5, PHP 7, PHP 8)

base64\_encode — Кодує дані у формат MIME base64

### Опис

```methodsynopsis
base64_encode(string $string): string
```

Кодує `string`с base64.

Це кодування призначене для коректної передачі бінарних даних за протоколами, які не підтримують 8-бітну передачу, наприклад, для відправлення тіла листа.

Дані, закодовані base64, займають на 33% більше місця в порівнянні з оригінальними даними.

### Список параметрів

`string`

Дані кодування.

### Значення, що повертаються

Кодовані дані у вигляді рядка.

### Приклади

**Пример #1 Пример использования**base64\_encode()\*\*\*\*

```php
<?php
$str = 'Это закодированная строка';
echo base64_encode($str);
?>
```

Результат виконання наведеного прикладу:

```
0K3RgtC+INC30LDQutC+0LTQuNGA0L7QstCw0L3QvdCw0Y8g0YHRgtGA0L7QutCw
```

### Дивіться також

-   [base64\_decode()](function.base64-decode.md) \- Декодує дані, закодовані MIME base64
-   [chunk\_split()](function.chunk-split.md) \- Розбиває рядок на фрагменти
-   [convert\_uuencode()](function.convert-uuencode.md) \- Кодує рядок у форматі uuencode
-   [» RFC 2045](http://www.faqs.org/rfcs/rfc2045)розділ 6.8
