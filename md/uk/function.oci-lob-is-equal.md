---
navigation:
  - function.oci-lob-copy.md: « ocilobcopy
  - function.oci-new-collection.md: ocinewcollection »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функции
title: ociлобісequal
---
# ociлобісequal

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ociлобісequal - Порівнює два об'єкти LOB/FILE

### Опис

```methodsynopsis
oci_lob_is_equal(OCILob $lob1, OCILob $lob2): bool
```

Порівнює два об'єкти LOB/FILE.

### Список параметрів

`lob1`

Ідентифікатор LOB.

`lob2`

Ідентифікатор LOB.

### Значення, що повертаються

Повертає **`true`**, якщо об'єкти ідентичні, та **`false`** у протилежному випадку або у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Клас OCILob називався OCI-Lob до PHP 8 та PECL OCI8 3.0.0.
