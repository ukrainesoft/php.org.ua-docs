Експортує файл CMS до масиву сертифікатів PEM

-   [« opensslcmsencrypt](function.openssl-cms-encrypt.html)
    
-   [opensslcmssign »](function.openssl-cms-sign.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Експортує файл CMS до масиву сертифікатів PEM
    

# opensslcmsread

(PHP 8)

opensslcmsread — Експортує файл CMS до масиву сертифікатів PEM

### Опис

```methodsynopsis
openssl_cms_read(string $input_filename, array &$certificates): bool
```

Працює аналогічно [opensslpkcs7read()](function.openssl-pkcs7-read.html)

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`input_filename`

`certificates`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.