---
navigation:
  - ocilob.flush.md: '« OCILob::flush'
  - ocilob.getbuffering.md: 'OCILob::getBuffering »'
  - index.md: PHP Manual
  - class.ocilob.md: OCILob
title: 'OCILob::free'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OCILob::free

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

OCILob::free — Звільняє ресурси, пов'язані з дескриптором LOB

### Опис

```methodsynopsis
public OCILob::free(): bool
```

Звільняє ресурси, пов'язані з дескриптором LOB, спочатку виділені функцією [oci\_new\_descriptor()](function.oci-new-descriptor.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Класс**OCI-Lob**перейменований на[OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |
