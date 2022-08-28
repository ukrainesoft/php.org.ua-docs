Експортує сертифікат у рядок

-   [« openssl\_x509\_export\_to\_file](function.openssl-x509-export-to-file.html)
    
-   [openssl\_x509\_fingerprint »](function.openssl-x509-fingerprint.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Експортує сертифікат у рядок
    

# opensslx509export

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

opensslx509export — Експортує сертифікат у рядок

### Опис

```methodsynopsis
openssl_x509_export(OpenSSLCertificate|string $certificate, string &$output, bool $no_text = true): bool
```

**opensslx509export()** зберігає сертифікат `certificate` у вигляді PEM рядка в `output`

### Список параметрів

`x509`

Для списку коректних значень дивіться [Параметры ключей/сертификатов](openssl.certparams.html)

`output`

У разі успішного виконання цієї змінної буде PEM-представлення сертифіката.

`no_text`

Необов'язковий параметр `notext` впливає на деталізацію повідомлень виводу; якщо він встановлений у **`false`**, то у висновок додається додаткова людина читана інформація. Значення за замовчуванням `notext` є **`true`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.html); раніше приймався ресурс ([resource](language.types.resource.html)) типу `OpenSSL X.509` |