Експортує до сумісного з PKCS#12 файлу сховища сертифікатів

-   [« openssl\_pbkdf2](function.openssl-pbkdf2.html)
    
-   [openssl\_pkcs12\_export »](function.openssl-pkcs12-export.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Експортує до сумісного з PKCS#12 файлу сховища сертифікатів
    

# opensslpkcs12exportтоfile

(PHP 5> = 5.2.2, PHP 7, PHP 8)

opensslpkcs12exportтоfile — Експортує сумісний з PKCS#12 файл сховища сертифікатів

### Опис

```methodsynopsis
openssl_pkcs12_export_to_file(    OpenSSLCertificate|string $certificate,    string $output_filename,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $private_key,    string $passphrase,    array $options = []): bool
```

**opensslpkcs12exportтоfile()** зберігає `certificate` у файл `output_filename` у форматі PKCS#12.

### Список параметрів

`x509`

Для списку коректних значень дивіться [Параметры ключей/сертификатов](openssl.certparams.html)

`output_filename`

Шлях до файлу.

`private_key`

Закритий компонент ключа PKCS#12. Допустимі значення дивіться [Параметры закрытого/открытого ключа](openssl.certparams.html)

`passphrase`

Пароль для розблокування PKCS#12.

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
|  | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.html); раніше приймався ресурс ([resource](language.types.resource.html)) типу `OpenSSL X.509 CSR` |
|  | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html) або [OpenSSLCertificate](class.opensslcertificate.html); раніше приймався ресурс ([resource](language.types.resource.html)) типу `OpenSSL key` або `OpenSSL X.509` |