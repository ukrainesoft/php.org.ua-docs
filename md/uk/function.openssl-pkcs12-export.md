Експортує сумісний з PKCS#12 файл сховища сертифікатів у змінну

-   [« opensslpkcs12exportтоfile](function.openssl-pkcs12-export-to-file.html)
    
-   [opensslpkcs12read »](function.openssl-pkcs12-read.html)
    
-   [PHP Manual](index.md)
    
-   [Функции OpenSSL](ref.openssl.md)
    
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

Для списку коректних значень дивіться [Параметри ключів/сертифікатів](openssl.certparams.md)

`output`

У разі успішного виконання міститиме PKCS#12.

`private_key`

Компонент закритого ключа PKCS#12. Список допустимих значень дивіться на сторінці [параметрів відкритого/закритого ключа](openssl.certparams.md)

`passphrase`

Пароль для шифрування PKCS#12.

`options`

Масив опцій. Ключі, які не описані тут, будуть проігноровані.

| Ключ | Описание |
| --- | --- |
| `"extracerts"` | масив додаткових сертифікатів або один сертифікат для включення файлу PKCS#12. |
| `"friendlyname"` | рядок для використання сертифікатом та ключем |

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL X.509 CSR` |
|  | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL key` або `OpenSSL X.509` |