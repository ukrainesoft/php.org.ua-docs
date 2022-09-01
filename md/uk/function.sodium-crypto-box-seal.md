---
navigation:
  - function.sodium-crypto-box-seal-open.html: « sodiumcryptoboxsealopen
  - function.sodium-crypto-box-secretkey.html: sodiumcryptoboxsecretkey »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptoboxseal
---
# sodiumcryptoboxseal

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoboxseal — Шифрування відкритим ключем без автентифікації

### Опис

```methodsynopsis
sodium_crypto_box_seal(string $message, string $public_key): string
```

Шифрує повідомлення так, що тільки одержувач може його розшифрувати.

На відміну від [sodiumcryptobox()](function.sodium-crypto-box.md)Вам потрібно знати тільки відкритий ключ одержувача, щоб використовувати **sodiumcryptoboxseal()**. Однак одним із наслідків цієї зручності є те, що зашифрований текст не прив'язаний до статичного відкритого ключа і, отже, не автентифікується. Отже, шифрування відкритим ключем без автентифікації.

**sodiumcryptoboxseal()** як і забезпечує цілісність зашифрованого тексту. Тільки не перевіряє справжність відправника.

Якщо вам також потрібна автентифікація відправника, найкраще почати з функцій [sodiumcryptosign()](function.sodium-crypto-sign.md)

### Список параметрів

`message`

Повідомлення, яке потрібно зашифрувати.

`public_key`

Відкритий ключ, який відповідає єдиному ключу, який може розшифрувати повідомлення.

### Значення, що повертаються

Рядок зашифрованого тексту (одноразовий відкритий ключ, зашифроване повідомлення, тег аутентифікації).

### Приклади

**Приклад #1 Приклад використання **sodiumcryptoboxseal()****

```php
<?php
$keypair = sodium_crypto_box_keypair();
$public_key = sodium_crypto_box_publickey($keypair);

// Обфусцированный текст, чтобы сделать пример более увлекательным
$plaintext_b64 = "V3JpdGluZyBzb2Z0d2FyZSBpbiBQSFAgY2FuIGJlIGEgZGVsaWdodCE=";
$decoded_plaintext = sodium_base642bin($plaintext_b64, SODIUM_BASE64_VARIANT_ORIGINAL);

$sealed = sodium_crypto_box_seal($decoded_plaintext, $public_key);
var_dump(base64_encode($sealed));

$opened = sodium_crypto_box_seal_open($sealed, $keypair);
var_dump($opened);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(120) "oRBXXAV4iQBrxlV4A21Bord8Yo/D8ZlrIIGNyaRCcGBfpz0map52I3xq6l+CST+1NSgQkbV+HiYyFjXWiWiaCGupGf+zl4bgWj/A9Adtem7Jt3h3emrMsLw="
string(41) "Writing software in PHP can be a delight!"
```
