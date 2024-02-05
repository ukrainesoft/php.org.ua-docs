---
navigation:
  - function.oci-field-type.md: « oci\_field\_type
  - function.oci-free-statement.md: oci\_free\_statement »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_free\_descriptor
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_free\_descriptor

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_free\_descriptor - Звільняє дескриптор

### Опис

```methodsynopsis
oci_free_descriptor(OCILob $lob): bool
```

Звільняє дескриптор, створений за допомогою [oci\_new\_descriptor()](function.oci-new-descriptor.md)

### Список параметрів

`descriptor`

Дескриптор, створений за допомогою [oci\_new\_descriptor()](function.oci-new-descriptor.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження** :
> 
> Функція зазвичай використовується як метод [OCILOB::free](ocilob.free.md)

### Дивіться також

-   [OCILOB::free](ocilob.free.md)
