---
navigation:
  - ref.url.md: « Функції URL
  - function.base64-encode.md: base64encode »
  - index.md: PHP Manual
  - ref.url.md: Функції URL
title: base64decode
---
# base64decode

(PHP 4, PHP 5, PHP 7, PHP 8)

base64decode — Декодує дані, закодовані MIME base64

### Опис

```methodsynopsis
base64_decode(string $string, bool $strict = false): string|false
```

Декодує рядок `string`, закодований за допомогою base64.

### Список параметрів

`string`

Закодовані дані.

`strict`

Якщо параметр `strict` заданий як **`true`**, функція **base64decode()** поверне **`false`** у випадку, якщо вхідні дані містять символи, що не входять до алфавіту base64. Інакше такі символи будуть відкинуті.

### Значення, що повертаються

Повертає декодовані дані або **`false`** у разі виникнення помилки. Повертаються можуть бути бінарними.

### Приклади

**Приклад #1 Приклад використання **base64decode()****

```php
<?php
$str = '0K3RgtC+INC30LDQutC+0LTQuNGA0L7QstCw0L3QvdCw0Y8g0YHRgtGA0L7QutCw';
echo base64_decode($str);
?>
```

Результат виконання цього прикладу:

```
Это закодированная строка
```

### Дивіться також

-   [base64encode()](function.base64-encode.md) - Кодує дані у формат MIME base64
-   [» RFC 2045](http://www.faqs.org/rfcs/rfc2045) розділ 6.8
