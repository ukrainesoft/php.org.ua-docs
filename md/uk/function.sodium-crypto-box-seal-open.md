---
navigation:
  - function.sodium-crypto-box-publickey.md: « sodium\_crypto\_box\_publickey
  - function.sodium-crypto-box-seal.md: sodium\_crypto\_box\_seal »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_box\_seal\_open
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_box\_seal\_open

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_box\_seal\_open — Розшифровка відкритим ключем без автентифікації

### Опис

```methodsynopsis
sodium_crypto_box_seal_open(string $ciphertext, string $key_pair): string|false
```

Розшифровує повідомлення, зашифроване за допомогою [sodium\_crypto\_box\_seal()](function.sodium-crypto-box-seal.md)

### Список параметрів

`ciphertext`

Зашифроване повідомлення

`key_pair`

Ключова пара отримувача. Повинна включати секретний ключ.

### Значення, що повертаються

Текст у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** sodium\_crypto\_box\_seal\_open()\*\*\*\*

```php
<?php
// Шифрованный текст нечувствителен; base64_decode в порядке
$sealed_b64 = "oRBXXAV4iQBrxlV4A21Bord8Yo/D8ZlrIIGNyaRCcGBfpz0map52I3xq6l+CST+1NSgQkbV+HiYyFjXWiWiaCGupGf+zl4bgWj/A9Adtem7Jt3h3emrMsLw=";
$sealed = base64_decode($sealed_b64);

// Ключевая пара содержит криптографический секрет; использовать безопасный по времени декодер
$keypair_b64 = "KZkF8wnB7bnC2aXB3lFOqCTc0Z6MllvaQb9ASVG8o2/MsewkuE4u1uaEgTzSakeiYyIW8DGj+02/L3cWIbs9bQ==";
$keypair = sodium_base642bin($keypair_b64, SODIUM_BASE64_VARIANT_ORIGINAL);

$opened = sodium_crypto_box_seal_open($sealed, $keypair);
var_dump($opened);
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(41) "Writing software in PHP can be a delight!"
```
