---
navigation:
  - function.openssl-encrypt.md: « openssl\_encrypt
  - function.openssl-free-key.md: openssl\_free\_key »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_error\_string
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_error\_string

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

openssl\_error\_string — Повертає повідомлення про помилку openSSL

### Опис

```methodsynopsis
openssl_error_string(): string|false
```

**openssl\_error\_string()** повертає повідомлення останньої помилки бібліотеки openSSL, що відбулася. Повідомлення про помилки знаходяться в черзі, тому цю функцію можна викликати кілька разів для отримання всієї інформації. При цьому останнє повідомлення найсвіжіше.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок з повідомленням про помилку або \*\*`false`\*\*якщо повідомлень більше немає.

### Приклади

**Пример #1 Пример использования**openssl\_error\_string()\*\*\*\*

```php
<?php
// Предположим, что вы вызвали функцию openssl, которая завершилась неудачей
while ($msg = openssl_error_string())
    echo $msg . "<br />\n";
?>
```
