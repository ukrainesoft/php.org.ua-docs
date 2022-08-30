Розбирає сховище сертифікатів PKCS#12 масив

-   [« opensslpkcs12export](function.openssl-pkcs12-export.html)
    
-   [opensslpkcs7decrypt »](function.openssl-pkcs7-decrypt.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Розбирає сховище сертифікатів PKCS#12 масив
    

# opensslpkcs12read

(PHP 5> = 5.2.2, PHP 7, PHP 8)

opensslpkcs12read — Розбирає сховище сертифікатів PKCS#12 у масив

### Опис

```methodsynopsis
openssl_pkcs12_read(string $pkcs12, array &$certificates, string $passphrase): bool
```

**opensslpkcs12read()** розбирає сховище сертифікатів PKCS#12, задане в `pkcs12` і поміщає в масив `certificates`

### Список параметрів

`pkcs12`

Вміст сховища сертифікатів, а не його ім'я.

`certificates`

У разі успішного виконання міститиме дані сховища сертифіката (Certificate Store Data).

`passphrase`

Пароль для розшифровки PKCS#12.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **opensslpkcs12read()****

```php
<?php
if (!$cert_store = file_get_contents("/certs/file.p12")) {
    echo "Ошибка: невозможно прочитать файл сертификата\n";
    exit;
}

if (openssl_pkcs12_read($cert_store, $cert_info, "my_secret_pass")) {
    echo "Информация об сертификате\n";
    print_r($cert_info);
} else {
    echo "Ошибка: невозможно прочитать хранилище сертификата.\n";
    exit;
}
?>
```