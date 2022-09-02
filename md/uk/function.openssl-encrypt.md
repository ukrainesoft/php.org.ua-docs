---
navigation:
  - function.openssl-digest.md: « openssldigest
  - function.openssl-error-string.md: opensslerrorstring »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslencrypt
---
# opensslencrypt

(PHP 5> = 5.3.0, PHP 7, PHP 8)

opensslencrypt - Шифрує дані

### Опис

```methodsynopsis
openssl_encrypt(    string $data,    string $cipher_algo,    string $passphrase,    int $options = 0,    string $iv = "",    string &$tag = null,    string $aad = "",    int $tag_length = 16): string|false
```

Шифрує дані із заданим шифром і ключем і повертає необроблений рядок або рядок, закодований у base64

### Список параметрів

`data`

Дані для шифрування.

`cipher_algo`

Метод шифрування. Список доступних методів можна отримати за допомогою функції [opensslgetciphermethods()](function.openssl-get-cipher-methods.md)

`passphrase`

Кодова фраза. Якщо кодова фраза вкорочена, ніж очікувалося, вона автоматично доповнюється символами `NUL`; якщо кодова фраза довша, ніж очікувалося, вона автоматично усікається.

`options`

`options` можна задати одній з констант: **`OPENSSL_RAW_DATA`** **`OPENSSL_ZERO_PADDING`**

`iv`

Ненульовий вектор, що ініціалізує.

`tag`

Тег аутентифікації, який передається за посиланням, у режимі шифрування AEAD (GCM або CCM).

`aad`

Додаткові автентифіковані дані.

`tag_length`

Довжина параметра `tag`. Для режиму GCM має бути від 4 до 16.

### Значення, що повертаються

Повертає зашифрований рядок або **`false`** у разі виникнення помилки.

### Помилки

Видає помилку рівня **`E_WARNING`**, якщо параметр `cipher_algo` передано невідомий алгоритм шифрування.

Видає помилку рівня **`E_WARNING`**, якщо параметр `iv` передано порожнє значення.

### список змін

| Версия | Описание |
| --- | --- |
|  | Додані параметри `tag` `aad` і `tag_length` |

### Приклади

**Приклад #1 Приклад шифрування AES з автентифікацією в режимі GCM PHP 7.1+**

```php
<?php
// $key должен быть сгенерирован заранее криптографически безопасным образом
// например, с помощью openssl_random_pseudo_bytes
$plaintext = "данные для шифрования";
$cipher = "aes-128-gcm";
if (in_array($cipher, openssl_get_cipher_methods()))
{
    $ivlen = openssl_cipher_iv_length($cipher);
    $iv = openssl_random_pseudo_bytes($ivlen);
    $ciphertext = openssl_encrypt($plaintext, $cipher, $key, $options=0, $iv, $tag);
    // сохраняем $cipher, $iv и $tag для дальнейшей расшифровки
    $original_plaintext = openssl_decrypt($ciphertext, $cipher, $key, $options=0, $iv, $tag);
    echo $original_plaintext."\n";
}
?>
```

**Приклад #2 Приклад шифрування AES з автентифікацією до PHP 7.1**

```php
<?php
// $key должен быть сгенерирован заранее криптографически безопасным образом
// например, с помощью openssl_random_pseudo_bytes
$plaintext = "данные для шифрования";
$ivlen = openssl_cipher_iv_length($cipher="AES-128-CBC");
$iv = openssl_random_pseudo_bytes($ivlen);
$ciphertext_raw = openssl_encrypt($plaintext, $cipher, $key, $options=OPENSSL_RAW_DATA, $iv);
$hmac = hash_hmac('sha256', $ciphertext_raw, $key, $as_binary=true);
$ciphertext = base64_encode( $iv.$hmac.$ciphertext_raw );

// расшифровка....
$c = base64_decode($ciphertext);
$ivlen = openssl_cipher_iv_length($cipher="AES-128-CBC");
$iv = substr($c, 0, $ivlen);
$hmac = substr($c, $ivlen, $sha2len=32);
$ciphertext_raw = substr($c, $ivlen+$sha2len);
$original_plaintext = openssl_decrypt($ciphertext_raw, $cipher, $key, $options=OPENSSL_RAW_DATA, $iv);
$calcmac = hash_hmac('sha256', $ciphertext_raw, $key, $as_binary=true);
if (hash_equals($hmac, $calcmac))// сравнение, не подверженное атаке по времени
{
    echo $original_plaintext."\n";
}
?>
```

### Дивіться також

-   [openssldecrypt()](function.openssl-decrypt.md) - Розшифровує дані
