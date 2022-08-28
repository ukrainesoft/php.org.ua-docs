Витягує відкритий ключ із сертифікату та готує його до використання

-   [« openssl\_pkey\_get\_private](function.openssl-pkey-get-private.html)
    
-   [openssl\_pkey\_new »](function.openssl-pkey-new.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Витягує відкритий ключ із сертифікату та готує його до використання
    

# opensslpkeygetpublic

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

opensslpkeygetpublic — Витягує відкритий ключ із сертифікату та готує його до використання.

### Опис

```methodsynopsis
openssl_pkey_get_public(OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $public_key): OpenSSLAsymmetricKey|false
```

**opensslpkeygetpublic()** витягує відкритий ключ з `public_key` та готує його до використання в інших функціях.

### Список параметрів

`public_key`

`public_key` може бути одним з:

1.  екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html)
2.  рядок виду file://path/to/file.pem. Файл повинен містити кодований у PEM сертифікат/публічний ключ (може містити і те, й інше).
3.  Відкритий ключ у форматі PEM.

### Значення, що повертаються

Повертає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція повертає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html); раніше повертався ресурс ([resource](language.types.resource.html)) типу `OpenSSL key` |
|  | `public_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html) або [OpenSSLCertificate](class.opensslcertificate.html); раніше приймався ресурс ([resource](language.types.resource.html)) типу `OpenSSL key` або `OpenSSL X.509` |