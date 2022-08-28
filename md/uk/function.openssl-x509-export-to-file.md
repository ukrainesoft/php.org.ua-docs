Експортує сертифікат у файл

-   [« openssl\_x509\_checkpurpose](function.openssl-x509-checkpurpose.html)
    
-   [openssl\_x509\_export »](function.openssl-x509-export.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Експортує сертифікат у файл
    

# opensslx509exportтоfile

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

opensslx509exportтоfile — Експортує сертифікат у файл

### Опис

```methodsynopsis
openssl_x509_export_to_file(OpenSSLCertificate|string $certificate, string $output_filename, bool $no_text = true): bool
```

**opensslx509exportтоfile()** зберігає сертифікат `certificate` у файл `output_filename` у вигляді рядка у форматі PEM.

### Список параметрів

`x509`

Для списку коректних значень дивіться [Параметры ключей/сертификатов](openssl.certparams.html)

`output_filename`

Шлях до файлу.

`no_text`

Необов'язковий параметр `notext` впливає на деталізацію повідомлень виводу; якщо він встановлений у **`false`**, то у висновок додається додаткова людиночитана інформація. Значення за замовчуванням `notext` є **`true`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                                           |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.html); раніше приймався ресурс ([resource](language.types.resource.html)) типу `OpenSSL X.509` |