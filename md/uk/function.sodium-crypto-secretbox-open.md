---
navigation:
  - function.sodium-crypto-secretbox-keygen.md: « sodium\_crypto\_secretbox\_keygen
  - function.sodium-crypto-secretbox.md: sodium\_crypto\_secretbox »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_secretbox\_open
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_secretbox\_open

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_secretbox\_open — Розшифровка за допомогою спільного ключа з автентифікацією

### Опис

```methodsynopsis
sodium_crypto_secretbox_open(string $ciphertext, string $nonce, string $key): string|false
```

Розшифровує зашифроване повідомлення симетричним (загальним) ключем.

### Список параметрів

`ciphertext`

Має бути у форматі, наданому [sodium\_crypto\_secretbox()](function.sodium-crypto-secretbox.md) (Зашифрований текст та тег, об'єднані).

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 24 байти. Це досить велика межа для випадкової генерації (наприклад, [random\_bytes()](function.random-bytes.md)

`key`

Ключ шифрування (256 біт).

### Значення, що повертаються

Розшифрований рядок у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

-   Викидається [SodiumException](class.sodiumexception.md)якщо довжина байтів параметра`nonce` відрізняється від [**`SODIUM_CRYPTO_SECRETBOX_NONCEBYTES`**](sodium.constants.md#constant.sodium-crypto-secretbox-noncebytes)(24 байти).
-   Викидається [SodiumException](class.sodiumexception.md)якщо довжина байтів параметра`key` відрізняється від [**`SODIUM_CRYPTO_SECRETBOX_KEYBYTES`**](sodium.constants.md#constant.sodium-crypto-secretbox-keybytes)(32 байти).

### Приклади

**Пример #1 Пример использования**sodium\_crypto\_secretbox\_open()\*\*\*\*

```php
<?php
// $key должен храниться в секрете.
$key = random_bytes(SODIUM_CRYPTO_SECRETBOX_KEYBYTES);
// Не используйте $nonce повторно с тем же ключом
$nonce = random_bytes(SODIUM_CRYPTO_SECRETBOX_NONCEBYTES);
$ciphertext = sodium_crypto_secretbox('message to be encrypted', $nonce, $key);

// Для расшифровки $ciphertext требуются те же имя и ключ.
$plaintext = sodium_crypto_secretbox_open($ciphertext, $nonce, $key);
if ($plaintext !== false) {
    echo $plaintext . PHP_EOL;
}
?>
```

Результат виконання наведеного прикладу:

```
message to be encrypted
```

### Дивіться також

-   [sodium\_crypto\_secretbox()](function.sodium-crypto-secretbox.md) \- Шифрування із загальним ключем з автентифікацією
-   [sodium\_crypto\_secretbox\_keygen()](function.sodium-crypto-secretbox-keygen.md) \- Створює випадковий ключ для sodium\_crypto\_secretbox
-   [random\_bytes()](function.random-bytes.md) \- Отримує криптографічно безпечні випадкові байти
