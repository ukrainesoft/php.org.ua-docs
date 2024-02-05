---
navigation:
  - function.openssl-cms-encrypt.md: « openssl\_cms\_encrypt
  - function.openssl-cms-sign.md: openssl\_cms\_sign »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_cms\_read
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_cms\_read

(PHP 8)

openssl\_cms\_read — Експортує файл CMS до масиву сертифікатів PEM

### Опис

```methodsynopsis
openssl_cms_read(string $input_filename, array &$certificates): bool
```

Працює аналогічно [openssl\_pkcs7\_read()](function.openssl-pkcs7-read.md)

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`input_filename`

`certificates`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
