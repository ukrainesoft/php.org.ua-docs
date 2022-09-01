---
navigation:
  - function.sodium-crypto-secretbox-open.html: « sodiumcryptosecretboxopen
  - function.sodium-crypto-secretstream-xchacha20poly1305-init-pull.html: sodiumcryptosecretstreamxchacha20poly1305initpull »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptosecretbox
---
# sodiumcryptosecretbox

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptosecretbox — Шифрування із загальним ключем із автентифікацією

### Опис

```methodsynopsis
sodium_crypto_secretbox(string $message, string $nonce, string $key): string
```

Шифрування повідомлення є симетричним (загальним) ключем.

### Список параметрів

`message`

Текстове повідомлення, яке потрібно зашифрувати.

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 24 байти. Це досить велика межа для випадкової генерації (наприклад, [randombytes()](function.random-bytes.html)

`key`

Ключ шифрування (256 біт).

### Значення, що повертаються

Повертає зашифрований рядок.

### Помилки

-   Викидається [SodiumException](class.sodiumexception.md)якщо довжина байтів параметра `nonce` відрізняється від [**`SODIUM_CRYPTO_SECRETBOX_NONCEBYTES`**](sodium.constants.html#constant.sodium-crypto-secretbox-noncebytes) (24 байти).
-   Викидається [SodiumException](class.sodiumexception.md)якщо довжина байтів параметра `key` відрізняється від [**`SODIUM_CRYPTO_SECRETBOX_KEYBYTES`**](sodium.constants.html#constant.sodium-crypto-secretbox-keybytes) (32 байти).
-   Викидає [SodiumException](class.sodiumexception.md) у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **sodiumcryptosecretbox()****

```php
<?php
// $key должен храниться в секрете.
$key = sodium_crypto_secretbox_keygen();
// Не используйте $nonce повторно с тем же ключом
$nonce = random_bytes(SODIUM_CRYPTO_SECRETBOX_NONCEBYTES);
$plaintext = "message to be encrypted";
$ciphertext = sodium_crypto_secretbox($plaintext, $nonce, $key);

var_dump(bin2hex($ciphertext));
// Для расшифровки $ciphertext требуются те же имя и ключ.
var_dump(sodium_crypto_secretbox_open($ciphertext, $nonce, $key));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(78) "3a1fa3e9f7b72ef8be51d40abf8e296c6899c185d07b18b4c93e7f26aa776d24c50852cd6b1076"
string(23) "message to be encrypted"
```

### Дивіться також

-   [sodiumcryptosecretboxopen()](function.sodium-crypto-secretbox-open.html) - Розшифрування з використанням загального ключа з автентичністю
-   [sodiumcryptosecretboxkeygen()](function.sodium-crypto-secretbox-keygen.html) - Створює випадковий ключ для sodiumcryptosecretbox
-   [randombytes()](function.random-bytes.html) - Генерує криптографічно безпечні псевдовипадкові байти
