---
navigation:
  - function.sodium-crypto-secretbox-keygen.html: « sodiumcryptosecretboxkeygen
  - function.sodium-crypto-secretbox.html: sodiumcryptosecretbox »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptosecretboxopen
---
# sodiumcryptosecretboxopen

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptosecretboxopen — Розшифровка за допомогою спільного ключа з автентифікацією

### Опис

```methodsynopsis
sodium_crypto_secretbox_open(string $ciphertext, string $nonce, string $key): string|false
```

Розшифровує зашифроване повідомлення симетричним ключом.

### Список параметрів

`ciphertext`

Має бути у форматі, наданому [sodiumcryptosecretbox()](function.sodium-crypto-secretbox.html) (Зашифрований текст та тег, об'єднані).

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 24 байти. Це досить велика межа для випадкової генерації (наприклад, [randombytes()](function.random-bytes.html)

`key`

Ключ шифрування (256 біт).

### Значення, що повертаються

Розшифрований рядок у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

-   Викидається [SodiumException](class.sodiumexception.md)якщо довжина байтів параметра `nonce` відрізняється від [**`SODIUM_CRYPTO_SECRETBOX_NONCEBYTES`**](sodium.constants.html#constant.sodium-crypto-secretbox-noncebytes) (24 байти).
-   Викидається [SodiumException](class.sodiumexception.md)якщо довжина байтів параметра `key` відрізняється від [**`SODIUM_CRYPTO_SECRETBOX_KEYBYTES`**](sodium.constants.html#constant.sodium-crypto-secretbox-keybytes) (32 байти).

### Приклади

**Приклад #1 Приклад використання **sodiumcryptosecretboxopen()****

```php
<?php
// $key должен храниться в секрете.
$key = random_bytes(SODIUM_CRYPTO_SECRETBOX_KEYBYTES);
// Не используйте $nonce повторно с тем же ключом
$nonce = random_bytes(SODIUM_CRYPTO_SECRETBOX_NONCEBYTES);
$ciphertext = sodium_crypto_secretbox('message to be encrypted', $nonce, $key);

// Для расшифровки $ciphertext требуются те же имя и ключ.
$plaintext = sodium_crypto_secretbox_open($ciphertext, $nonce, $key);
if ($plaintext !== false) {
    echo $plaintext . PHP_EOL;
}
?>
```

Результат виконання цього прикладу:

```
message to be encrypted
```

### Дивіться також

-   [sodiumcryptosecretbox()](function.sodium-crypto-secretbox.html) - Шифрування із загальним ключем з автентифікацією
-   [sodiumcryptosecretboxkeygen()](function.sodium-crypto-secretbox-keygen.html) - Створює випадковий ключ для sodiumcryptosecretbox
-   [randombytes()](function.random-bytes.html) - Генерує криптографічно безпечні псевдовипадкові байти
