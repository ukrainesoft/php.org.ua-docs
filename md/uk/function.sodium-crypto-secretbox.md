---
navigation:
  - function.sodium-crypto-secretbox-open.md: « sodium\_crypto\_secretbox\_open
  - function.sodium-crypto-secretstream-xchacha20poly1305-init-pull.md: sodium\_crypto\_secretstream\_xchacha20poly1305\_init\_pull »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_secretbox
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_secretbox

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_secretbox — Шифрування із загальним ключем із автентифікацією

### Опис

```methodsynopsis
sodium_crypto_secretbox(string $message, string $nonce, string $key): string
```

Шифрування повідомлення є симетричним (загальним) ключем.

### Список параметрів

`message`

Текстове повідомлення, яке потрібно зашифрувати.

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 24 байти. Це досить велика межа для випадкової генерації (наприклад, [random\_bytes()](function.random-bytes.md)

`key`

Ключ шифрування (256 біт).

### Значення, що повертаються

Повертає зашифрований рядок.

### Помилки

-   Викидається [SodiumException](class.sodiumexception.md)якщо довжина байтів параметра`nonce` відрізняється від [**`SODIUM_CRYPTO_SECRETBOX_NONCEBYTES`**](sodium.constants.md#constant.sodium-crypto-secretbox-noncebytes)(24 байти).
-   Викидається [SodiumException](class.sodiumexception.md)якщо довжина байтів параметра`key` відрізняється від [**`SODIUM_CRYPTO_SECRETBOX_KEYBYTES`**](sodium.constants.md#constant.sodium-crypto-secretbox-keybytes)(32 байти).
-   Викидає [SodiumException](class.sodiumexception.md)в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** sodium\_crypto\_secretbox()\*\*\*\*

```php
<?php
// $key должен храниться в секрете.
$key = sodium_crypto_secretbox_keygen();
// Не используйте $nonce повторно с тем же ключом
$nonce = random_bytes(SODIUM_CRYPTO_SECRETBOX_NONCEBYTES);
$plaintext = "message to be encrypted";
$ciphertext = sodium_crypto_secretbox($plaintext, $nonce, $key);

var_dump(bin2hex($ciphertext));
// Для расшифровки $ciphertext требуются те же имя и ключ.
var_dump(sodium_crypto_secretbox_open($ciphertext, $nonce, $key));
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(78) "3a1fa3e9f7b72ef8be51d40abf8e296c6899c185d07b18b4c93e7f26aa776d24c50852cd6b1076"
string(23) "message to be encrypted"
```

### Дивіться також

-   [sodium\_crypto\_secretbox\_open()](function.sodium-crypto-secretbox-open.md) \- Розшифрування з використанням загального ключа з автентичністю
-   [sodium\_crypto\_secretbox\_keygen()](function.sodium-crypto-secretbox-keygen.md) \- Створює випадковий ключ для sodium\_crypto\_secretbox
-   [random\_bytes()](function.random-bytes.md) \- Отримує криптографічно безпечні випадкові байти
