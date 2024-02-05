---
navigation:
  - ocilob.read.md: '« OCILob::read'
  - ocilob.save.md: 'OCILob::save »'
  - index.md: PHP Manual
  - class.ocilob.md: OCILob
title: 'OCILob::rewind'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OCILob::rewind

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

OCILob::rewind — Переводить вказівник об'єкта на початок великого об'єкта

### Опис

```methodsynopsis
public OCILob::rewind(): bool
```

Встановлює внутрішній покажчик на початок об'єкта LOB.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Класс**OCI-Lob**перейменований на[OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::seek](ocilob.seek.md)
-   [OCILob::tell](ocilob.tell.md)
