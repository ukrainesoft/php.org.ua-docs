Шифрування даних відкритим ключем

-   [« openssl\_public\_decrypt](function.openssl-public-decrypt.html)
    
-   [openssl\_random\_pseudo\_bytes »](function.openssl-random-pseudo-bytes.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Шифрування даних відкритим ключем
    

# opensslpublicencrypt

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

opensslpublicencrypt — Шифрування даних відкритим ключем

### Опис

```methodsynopsis
openssl_public_encrypt(    string $data,    string &$encrypted_data,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $public_key,    int $padding = OPENSSL_PKCS1_PADDING): bool
```

**opensslpublicencrypt()** шифрує `data` відкритим ключем `public_key` і зберігає в `encrypted_data`. Згодом розшифрувати їх можна функцією [openssl\_private\_decrypt()](function.openssl-private-decrypt.html)

Ця функція використовується, наприклад, для надсилання повідомлень, які може прочитати тільки власник закритого ключа і ніхто більше. Також її можна використовуватиме шифрування інформації у базі даних.

### Список параметрів

`data`

`encrypted_data`

Міститиме результат шифрування.

`public_key`

Відкритий ключ.

`padding`

`padding` може бути однією з констант: **`OPENSSL_PKCS1_PADDING`** **`OPENSSL_SSLV23_PADDING`** **`OPENSSL_PKCS1_OAEP_PADDING`** **`OPENSSL_NO_PADDING`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `public_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html) або [OpenSSLCertificate](class.opensslcertificate.html); раніше приймався ресурс ([resource](language.types.resource.html)) типу `OpenSSL key` або `OpenSSL X.509` |

### Дивіться також

-   [openssl\_private\_encrypt()](function.openssl-private-encrypt.html) - Шифрує дані секретним ключем
-   [openssl\_private\_decrypt()](function.openssl-private-decrypt.html) - Розшифровує дані за допомогою закритого ключа