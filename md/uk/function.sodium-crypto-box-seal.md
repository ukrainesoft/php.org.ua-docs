---
navigation:
  - function.sodium-crypto-box-seal-open.md: « sodium\_crypto\_box\_seal\_open
  - function.sodium-crypto-box-secretkey.md: sodium\_crypto\_box\_secretkey »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_box\_seal
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_box\_seal

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_box\_seal — Шифрування відкритим ключем без автентифікації

### Опис

```methodsynopsis
sodium_crypto_box_seal(string $message, string $public_key): string
```

Шифрує повідомлення так, що тільки одержувач може його розшифрувати.

В отличие от[sodium\_crypto\_box()](function.sodium-crypto-box.md)Вам потрібно знати тільки відкритий ключ одержувача, щоб використовувати **sodium\_crypto\_box\_seal()**. Однак одним із наслідків цієї зручності є те, що зашифрований текст не прив'язаний до статичного відкритого ключа і, отже, не автентифікується. Отже, шифрування відкритим ключем без автентифікації.

**sodium\_crypto\_box\_seal()** як і забезпечує цілісність зашифрованого тексту. Тільки не перевіряє справжність відправника.

Якщо вам також потрібна автентифікація відправника, найкраще почати з функцій [sodium\_crypto\_sign()](function.sodium-crypto-sign.md)

### Список параметрів

`message`

Повідомлення, яке потрібно зашифрувати.

`public_key`

Відкритий ключ, який відповідає єдиному ключу, який може розшифрувати повідомлення.

### Значення, що повертаються

Рядок зашифрованого тексту (одноразовий відкритий ключ, зашифроване повідомлення, тег аутентифікації).

### Приклади

**Пример #1 Пример использования**sodium\_crypto\_box\_seal()\*\*\*\*

```php
<?php
$keypair = sodium_crypto_box_keypair();
$public_key = sodium_crypto_box_publickey($keypair);

// Обфусцированный текст, чтобы сделать пример более увлекательным
$plaintext_b64 = "V3JpdGluZyBzb2Z0d2FyZSBpbiBQSFAgY2FuIGJlIGEgZGVsaWdodCE=";
$decoded_plaintext = sodium_base642bin($plaintext_b64, SODIUM_BASE64_VARIANT_ORIGINAL);

$sealed = sodium_crypto_box_seal($decoded_plaintext, $public_key);
var_dump(base64_encode($sealed));

$opened = sodium_crypto_box_seal_open($sealed, $keypair);
var_dump($opened);
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(120) "oRBXXAV4iQBrxlV4A21Bord8Yo/D8ZlrIIGNyaRCcGBfpz0map52I3xq6l+CST+1NSgQkbV+HiYyFjXWiWiaCGupGf+zl4bgWj/A9Adtem7Jt3h3emrMsLw="
string(41) "Writing software in PHP can be a delight!"
```
