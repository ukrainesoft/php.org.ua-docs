---
navigation:
  - function.oci-statement-type.md: « oci\_statement\_type
  - class.ocicollection.md: OCICollection »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_unregister\_taf\_callback
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_unregister\_taf\_callback

(PHP 7.0 >= 7.0.23, PHP 8, PHP 7 >= 7.1.9, PHP 8, PECL OCI8 >= 2.1.7)

oci\_unregister\_taf\_callback — Видалити реєстрацію користувача callback-функції для Oracle Database TAF

### Опис

```methodsynopsis
oci_unregister_taf_callback(resource $connection): bool
```

Видаляє реєстрацію користувача callback-функції, зареєстровану для з'єднання `connection` за допомогою [oci\_register\_taf\_callback()](function.oci-register-taf-callback.md)Более подробно читайте[OCI8 Transparent Application Failover (TAF) Support](oci8.taf.md)

### Список параметрів

`connection`

Ідентифікатор з'єднання Oracle.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [oci\_register\_taf\_callback()](function.oci-register-taf-callback.md) \- Реєструє функцію зворотного виклику для Oracle Database TAF
