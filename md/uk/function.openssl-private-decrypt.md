Розшифровує дані за допомогою закритого ключа

-   [« opensslpkeynew](function.openssl-pkey-new.html)
    
-   [opensslprivateencrypt »](function.openssl-private-encrypt.html)
    
-   [PHP Manual](index.md)
    
-   [Функции OpenSSL](ref.openssl.md)
    
-   Розшифровує дані за допомогою закритого ключа
    

# opensslprivatedecrypt

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

opensslprivatedecrypt — Розшифровує дані за допомогою закритого ключа

### Опис

```methodsynopsis
openssl_private_decrypt(    string $data,    string &$decrypted_data,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $private_key,    int $padding = OPENSSL_PKCS1_PADDING): bool
```

**opensslprivatedecrypt()** розшифровує дані `data`, які раніше були зашифровані за допомогою [opensslpublicencrypt()](function.openssl-public-encrypt.html) і зберігає результат у `decrypted_data`

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

| Версия | Описание |
| --- | --- |
|  | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL key` або `OpenSSL X.509` |

### Дивіться також

-   [opensslpublicencrypt()](function.openssl-public-encrypt.html) - Шифрування даних відкритим ключем
-   [opensslpublicdecrypt()](function.openssl-public-decrypt.html) - Розшифрування даних за допомогою відкритого ключа