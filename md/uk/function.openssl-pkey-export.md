Отримує рядок із ключем у форматі PEM

-   [« openssl\_pkey\_export\_to\_file](function.openssl-pkey-export-to-file.html)
    
-   [openssl\_pkey\_free »](function.openssl-pkey-free.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Отримує рядок із ключем у форматі PEM
    

# opensslpkeyexport

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

opensslpkeyexport — Отримує рядок із ключем у форматі PEM

### Опис

```methodsynopsis
openssl_pkey_export(    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $key,    string &$output,    ?string $passphrase = null,    ?array $options = null): bool
```

**opensslpkeyexport()** експортує `key` у вигляді рядка у форматі PEM і зберігає його в `output` (Передається за посиланням).

> **Зауваження**: Для коректної роботи цієї функції має бути правильний openssl.cnf. Для більш детальної інформації дивіться зауваження під [разделом установки](openssl.installation.html)

### Список параметрів

`key`

`output`

`passphrase`

Ключ опціонально захищається паролем `passphrase`

`options`

`options` можна використовувати для тонкого налаштування процесу експорту шляхом вказівки або перевизначення опцій конфігураційного файлу openssl. Дивіться опис [openssl\_csr\_new()](function.openssl-csr-new.html) для детальної інформації про `options`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                                                                                                                 |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | `key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html) або [OpenSSLCertificate](class.opensslcertificate.html); раніше приймався ресурс ([resource](language.types.resource.html)) типу `OpenSSL key` або `OpenSSL X.509` |