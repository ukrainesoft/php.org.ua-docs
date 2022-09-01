---
navigation:
  - function.openssl-cms-encrypt.html: « opensslcmsencrypt
  - function.openssl-cms-sign.html: opensslcmssign »
  - index.html: PHP Manual
  - ref.openssl.html: Функции OpenSSL
title: opensslcmsread
---
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
