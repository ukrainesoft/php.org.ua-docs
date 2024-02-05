---
navigation:
  - function.openssl-pkey-get-public.md: « openssl\_pkey\_get\_public
  - function.openssl-private-decrypt.md: openssl\_private\_decrypt »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_pkey\_new
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_pkey\_new

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

openssl\_pkey\_new — Генерує новий закритий ключ

### Опис

```methodsynopsis
openssl_pkey_new(?array $options = null): OpenSSLAsymmetricKey|false
```

**openssl\_pkey\_new()** створює новий закритий ключ. Як отримати відкриту частину ключа показано на прикладі нижче.

> **Зауваження**: Для коректної роботи цієї функції має бути правильний openssl.cnf. Для більш детальної інформації дивіться зауваження під [розділом установки](openssl.installation.md)

### Список параметрів

`options`

Ви можете налаштувати параметри генерації ключа (наприклад, вказати число біт) за допомогою `options`Смотрите описание функции[openssl\_csr\_new()](function.openssl-csr-new.md) для детальної інформації про `options`

### Значення, що повертаються

Повертає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md), либо\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція повертає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md); раніше повертався ресурс ([resource](language.types.resource.md)) типу`OpenSSL key` |
| 7.1.0 | Доданий ключ `curve_name` option для забезпечення можливості створення EC ключів. |

### Приклади

**Приклад #1 Отримати відкриту частину ключа із закритого ключа**

```php
<?php
$private_key = openssl_pkey_new();
$public_key_pem = openssl_pkey_get_details($private_key)['key'];
echo $public_key_pem;
$public_key = openssl_pkey_get_public($public_key_pem);
var_dump($public_key);
?>
```

Висновок наведеного прикладу буде схожим на:

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
