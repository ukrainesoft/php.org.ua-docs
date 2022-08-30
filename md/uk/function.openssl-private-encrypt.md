Шифрує дані секретним ключем

-   [« opensslprivatedecrypt](function.openssl-private-decrypt.html)
    
-   [opensslpublicdecrypt »](function.openssl-public-decrypt.html)
    
-   [PHP Manual](index.md)
    
-   [Функции OpenSSL](ref.openssl.md)
    
-   Шифрує дані секретним ключем
    

# opensslprivateencrypt

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

opensslprivateencrypt - Шифрує дані секретним ключем

### Опис

```methodsynopsis
openssl_private_encrypt(    string $data,    string &$encrypted_data,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $private_key,    int $padding = OPENSSL_PKCS1_PADDING): bool
```

**opensslprivateencrypt()** шифрує `data` за допомогою секретного ключа `private_key` і зберігає результат у `encrypted_data`. Далі можна розшифрувати за допомогою [opensslpublicdecrypt()](function.openssl-public-decrypt.html)

Ця функція використовується, наприклад, для підпису даних. Щоб була впевненість у тому, хто саме надіслав повідомлення.

### Список параметрів

`data`

`encrypted_data`

`private_key`

`padding`

`padding` може бути однією з констант: **`OPENSSL_PKCS1_PADDING`** **`OPENSSL_NO_PADDING`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL key` або `OpenSSL X.509` |

### Дивіться також

-   [opensslpublicencrypt()](function.openssl-public-encrypt.html) - Шифрування даних відкритим ключем
-   [opensslpublicdecrypt()](function.openssl-public-decrypt.html) - Розшифрування даних за допомогою відкритого ключа