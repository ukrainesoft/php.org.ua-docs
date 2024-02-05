---
navigation:
  - function.openssl-cipher-iv-length.md: « openssl\_cipher\_iv\_length
  - function.openssl-cms-decrypt.md: openssl\_cms\_decrypt »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_cipher\_key\_length
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_cipher\_key\_length

(PHP 8 >= 8.2.0)

openssl\_cipher\_key\_length — Отримує довжину ключа шифрування

### Опис

```methodsynopsis
openssl_cipher_key_length(string $cipher_algo): int|false
```

Отримує довжину ключа шифрування.

### Список параметрів

`cipher_algo`

Метод шифрування, список можливих значень дивіться в описі функції [openssl\_get\_cipher\_methods()](function.openssl-get-cipher-methods.md)

### Значення, що повертаються

Повертає довжину шифру у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Видає помилку рівня \*\*`E_WARNING`\*\*якщо алгоритм шифрування невідомий.

### Приклади

**Пример #1 Пример использования**openssl\_cipher\_key\_length()\*\*\*\*

```php
<?php
$method = 'AES-128-CBC';

var_dump(openssl_cipher_key_length($method));
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(16)
```
