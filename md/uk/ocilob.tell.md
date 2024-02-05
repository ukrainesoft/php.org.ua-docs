---
navigation:
  - ocilob.size.md: '« OCILob::size'
  - ocilob.truncate.md: 'OCILob::truncate »'
  - index.md: PHP Manual
  - class.ocilob.md: OCILob
title: 'OCILob::tell'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OCILob::tell

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

OCILob::tell — Повертає поточну позицію внутрішнього покажчика об'єкта LOB

### Опис

```methodsynopsis
public OCILob::tell(): int|false
```

Повертає поточну позицію внутрішнього покажчика об'єкта LOB.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає поточну позицію внутрішнього покажчика об'єкта LOB або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Класс**OCI-Lob**перейменований на[OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::rewind](ocilob.rewind.md)
-   [OCILob::size](ocilob.size.md)
-   [OCILob::eof](ocilob.eof.md)
