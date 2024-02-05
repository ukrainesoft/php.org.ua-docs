---
navigation:
  - ref.openssl.md: « Функції OpenSSL
  - function.openssl-cipher-key-length.md: openssl\_cipher\_key\_length »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_cipher\_iv\_length
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_cipher\_iv\_length

(PHP 5 >= 5.3.3, PHP 7, PHP 8)

openssl\_cipher\_iv\_length — Отримує довжину вектора, що ініціалізує, шифру.

### Опис

```methodsynopsis
openssl_cipher_iv_length(string $cipher_algo): int|false
```

Повертає довжину шифру, що ініціалізує вектор.

### Список параметрів

`cipher_algo`

Метод шифрування. Список потенційних значень можна отримати за допомогою [openssl\_get\_cipher\_methods()](function.openssl-get-cipher-methods.md)

### Значення, що повертаються

Повертає довжину вектора, що ініціалізує, шифру або **`false`**

### Помилки

Видає помилку рівня **`E_WARNING`** у разі передачі невідомого алгоритму шифрування.

### Приклади

**Приклад #1 Приклад використання** openssl\_cipher\_iv\_length()\*\*\*\*

```php
<?php
$method = 'AES-128-CBC';
$ivlen = openssl_cipher_iv_length($method);

echo $ivlen;
?>
```

Висновок наведеного прикладу буде схожим на:

```
16
```
