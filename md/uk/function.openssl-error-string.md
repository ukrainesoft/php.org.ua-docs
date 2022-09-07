---
navigation:
  - function.openssl-encrypt.md: « opensslencrypt
  - function.openssl-free-key.md: opensslfreekey »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslerrorstring
---
# opensslerrorstring

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

opensslerrorstring — Повертає повідомлення про помилку openSSL

### Опис

```methodsynopsis
openssl_error_string(): string|false
```

**opensslerrorstring()** повертає повідомлення останньої помилки бібліотеки openSSL, що відбулася. Повідомлення про помилки знаходяться в черзі, тому цю функцію можна викликати кілька разів для отримання всієї інформації. При цьому останнє повідомлення найсвіжіше.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок з повідомленням про помилку або \*\*`false`\*\*якщо повідомлень більше немає.

### Приклади

**Приклад #1 Приклад використання **opensslerrorstring()****

```php
<?php
// Предположим, что вы вызвали функцию openssl, которая завершилась неудачей
while ($msg = openssl_error_string())
    echo $msg . "<br />\n";
?>
```
