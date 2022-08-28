Генерує новий закритий ключ

-   [« openssl\_pkey\_get\_public](function.openssl-pkey-get-public.html)
    
-   [openssl\_private\_decrypt »](function.openssl-private-decrypt.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Генерує новий закритий ключ
    

# opensslpkeynew

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

opensslpkeynew — Генерує новий закритий ключ

### Опис

```methodsynopsis
openssl_pkey_new(?array $options = null): OpenSSLAsymmetricKey|false
```

**opensslpkeynew()** створює новий закритий ключ. Як отримати відкриту частину ключа показано на прикладі нижче.

> **Зауваження**: Для коректної роботи цієї функції має бути правильний openssl.cnf. Для більш детальної інформації дивіться зауваження під [разделом установки](openssl.installation.html)

### Список параметрів

`options`

Ви можете налаштувати параметри генерації ключа (наприклад, вказати число біт) за допомогою `options`. Дивіться опис функції [openssl\_csr\_new()](function.openssl-csr-new.html) для детальної інформації про `options`

### Значення, що повертаються

Повертає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html), або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                                                              |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | У разі успішного виконання функція повертає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html); раніше повертався ресурс ([resource](language.types.resource.html)) типу `OpenSSL key` |
|        | Доданий ключ `curve_name` option для забезпечення можливості створення EC ключів.                                                                                                                     |

### Приклади

**Приклад #1 Отримати відкриту частину ключа із закритого ключа**

```php
<?php
$private_key = openssl_pkey_new();
$public_key_pem = openssl_pkey_get_details($private_key)['key'];
echo $public_key_pem;
$public_key = openssl_pkey_get_public($public_key_pem);
var_dump($public_key);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
-----BEGIN PUBLIC KEY-----
MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEArZFsmN2P6rx1Xt7YV95o
gcdlal0k3ryiIhFNzjwtRNNTXfEfBr6lUuaIJYQ8/XqEBX0hpcfuuF6tTRlonA3t
WLME0QFD93YVsAaXcy76YqjjqcRRodIBphAbYyyMI/lXkQAdn7kbAmr7neSOsMYJ
El9Wo4Hl4oG6e52ZnYHyqW9dxh4hX93eupR2TmcCdVf+r9xoHewP0KJYSHt7vDUX
AQlWYcQiWHIadFsmL0orr6mutlXFReoHbesgKY9/3YLOu0JfxflSjIZ2JeL1NTl1
MsmODsUwgAUrwnWKKx+eQUP5g3GnSB3dPkRh9zRVRiLNWbCugyjrf3e6DgQWrW7j
pwIDAQAB
-----END PUBLIC KEY-----
resource(5) of type (OpenSSL key)
```