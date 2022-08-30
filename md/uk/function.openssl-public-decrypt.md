Розшифрування даних за допомогою відкритого ключа

-   [« opensslprivateencrypt](function.openssl-private-encrypt.html)
    
-   [opensslpublicencrypt »](function.openssl-public-encrypt.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Розшифрування даних за допомогою відкритого ключа
    

# opensslpublicdecrypt

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

opensslpublicdecrypt — Розшифровування даних за допомогою відкритого ключа

### Опис

```methodsynopsis
openssl_public_decrypt(    string $data,    string &$decrypted_data,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $public_key,    int $padding = OPENSSL_PKCS1_PADDING): bool
```

**opensslpublicdecrypt()** розшифровує дані `data`, які раніше були зашифровані за допомогою [opensslprivateencrypt()](function.openssl-private-encrypt.html) і зберігає результат у `decrypted_data`

Ви можете використовувати цю функцію, наприклад, щоб перевірити, чи було повідомлення написане власником закритого ключа.

### Список параметрів

`data`

`decrypted_data`

`public_key`

`public_key` повинен мати відповідний відкритий ключ.

`padding`

`padding` може бути однією з констант: **`OPENSSL_PKCS1_PADDING`** **`OPENSSL_NO_PADDING`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `public_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html) або [OpenSSLCertificate](class.opensslcertificate.html); раніше приймався ресурс ([resource](language.types.resource.html)) типу `OpenSSL key` або `OpenSSL X.509` |

### Дивіться також

-   [opensslprivateencrypt()](function.openssl-private-encrypt.html) - Шифрує дані секретним ключем
-   [opensslprivatedecrypt()](function.openssl-private-decrypt.html) - Розшифровує дані за допомогою закритого ключа