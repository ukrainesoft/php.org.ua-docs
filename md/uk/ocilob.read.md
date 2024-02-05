---
navigation:
  - ocilob.load.md: '« OCILob::load'
  - ocilob.rewind.md: 'OCILob::rewind »'
  - index.md: PHP Manual
  - class.ocilob.md: OCILob
title: 'OCILob::read'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OCILob::read

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

OCILob::read — Повертає частину об'єкта LOB

### Опис

```methodsynopsis
public OCILob::read(int $length): string|false
```

Читає `length` байтів (BLOB) або символів (CLOB) із поточної позиції об'єкта LOB.

Чтение останавливается, когда прочитано`length`байтов для BLOB,`length` символів для CLOB або коли досягнуто кінець об'єкта. Внутрішній покажчик об'єкта буде зрушено на кількість прочитаних байт/символів.

### Список параметрів

`length`

Довжина даних, що зчитуються, в байтах (BLOB) або символах (CLOB). Великі значення округляються до 1 MB.

### Значення, що повертаються

Повертає вміст у вигляді рядка або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Класс**OCI-Lob**перейменований на[OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::load](ocilob.load.md)
-   [OCILob::write](ocilob.write.md)
