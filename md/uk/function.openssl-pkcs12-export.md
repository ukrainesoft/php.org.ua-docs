Експортує сумісний з PKCS#12 файл сховища сертифікатів у змінну

-   [« openssl\_pkcs12\_export\_to\_file](function.openssl-pkcs12-export-to-file.html)
    
-   [openssl\_pkcs12\_read »](function.openssl-pkcs12-read.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Експортує сумісний з PKCS#12 файл сховища сертифікатів у змінну
    

# opensslpkcs12export

(PHP 5> = 5.2.2, PHP 7, PHP 8)

opensslpkcs12export — Експортує сумісний із PKCS#12 файл сховища сертифікатів у змінну

### Опис

```methodsynopsis
openssl_pkcs12_export(    OpenSSLCertificate|string $certificate,    string &$output,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $private_key,    string $passphrase,    array $options = []): bool
```

**opensslpkcs12export()** зберігає `x509` у змінну `out` у форматі PKCS#12.

### Список параметрів

`x509`

Для списку коректних значень дивіться [Параметры ключей/сертификатов](openssl.certparams.html)

`output`

У разі успішного виконання міститиме PKCS#12.

`private_key`

Компонент закритого ключа PKCS#12. Список допустимих значень дивіться на сторінці [параметров открытого/закрытого ключа](openssl.certparams.html)

`passphrase`

Пароль для шифрування PKCS#12.

`options`

Масив опцій. Ключі, які не описані тут, будуть проігноровані.

| Ключ             | Описание                                                                       |
|------------------|--------------------------------------------------------------------------------|
| `"extracerts"`   | масив додаткових сертифікатів або один сертифікат для включення файлу PKCS#12. |
| `"friendlyname"` | рядок для використання сертифікатом та ключем                                  |

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                                                                                                                         |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.html); раніше приймався ресурс ([resource](language.types.resource.html)) типу `OpenSSL X.509 CSR`                                                                           |
|        | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html) або [OpenSSLCertificate](class.opensslcertificate.html); раніше приймався ресурс ([resource](language.types.resource.html)) типу `OpenSSL key` або `OpenSSL X.509` |