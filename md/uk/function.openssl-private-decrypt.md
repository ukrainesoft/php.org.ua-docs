Розшифровує дані за допомогою закритого ключа

-   [« openssl\_pkey\_new](function.openssl-pkey-new.html)
    
-   [openssl\_private\_encrypt »](function.openssl-private-encrypt.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Розшифровує дані за допомогою закритого ключа
    

# opensslprivatedecrypt

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

opensslprivatedecrypt — Розшифровує дані за допомогою закритого ключа

### Опис

```methodsynopsis
openssl_private_decrypt(    string $data,    string &$decrypted_data,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $private_key,    int $padding = OPENSSL_PKCS1_PADDING): bool
```

**opensslprivatedecrypt()** розшифровує дані `data`, які раніше були зашифровані за допомогою [openssl\_public\_encrypt()](function.openssl-public-encrypt.html) і зберігає результат у `decrypted_data`

Ви можете використовувати цю функцію, наприклад, для розшифровування даних, які повинні бути доступні тільки вам і більше.

### Список параметрів

`data`

`decrypted_data`

`private_key`

`private_key` має бути секретним ключем, що відповідає тому, чим ми шифрували дані.

`padding`

`padding` може приймати одне з наступних значень: **`OPENSSL_PKCS1_PADDING`** **`OPENSSL_SSLV23_PADDING`** **`OPENSSL_PKCS1_OAEP_PADDING`** **`OPENSSL_NO_PADDING`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                                                                                                                         |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html) або [OpenSSLCertificate](class.opensslcertificate.html); раніше приймався ресурс ([resource](language.types.resource.html)) типу `OpenSSL key` або `OpenSSL X.509` |

### Дивіться також

-   [openssl\_public\_encrypt()](function.openssl-public-encrypt.html) - Шифрування даних відкритим ключем
-   [openssl\_public\_decrypt()](function.openssl-public-decrypt.html) - Розшифрування даних за допомогою відкритого ключа