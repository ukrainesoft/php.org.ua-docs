---
navigation:
  - ref.openssl.md: « Функции OpenSSL
  - function.openssl-cms-decrypt.html: opensslcmsdecrypt »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslcipherвербlength
---
# opensslcipherвербlength

(PHP 5> = 5.3.3, PHP 7, PHP 8)

opensslcipherвербlength — Отримує довжину вектора, що ініціалізує, шифру.

### Опис

```methodsynopsis
openssl_cipher_iv_length(string $cipher_algo): int|false
```

Повертає довжину шифру, що ініціалізує вектор.

### Список параметрів

`cipher_algo`

Метод шифрування. Список потенційних значень можна отримати за допомогою [opensslgetciphermethods()](function.openssl-get-cipher-methods.html)

### Значення, що повертаються

Повертає довжину вектора, що ініціалізує, шифру або **`false`**

### Помилки

Видає помилку рівня **`E_WARNING`** у разі передачі невідомого алгоритму шифрування.

### Приклади

**Приклад #1 Приклад використання **opensslcipherвербlength()****

```php
<?php
$method = 'AES-128-CBC';
$ivlen = openssl_cipher_iv_length($method);

echo $ivlen;
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
16
```
