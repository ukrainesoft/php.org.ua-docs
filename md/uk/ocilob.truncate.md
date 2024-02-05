---
navigation:
  - ocilob.tell.md: '« OCILob::tell'
  - ocilob.write.md: 'OCILob::write »'
  - index.md: PHP Manual
  - class.ocilob.md: OCILob
title: 'OCILob::truncate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OCILob::truncate

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

OCILob::truncate — Обрізає великий об'єкт

### Опис

```methodsynopsis
public OCILob::truncate(int $length = 0): bool
```

Обрізає об'єкт LOB.

### Список параметрів

`length`

Якщо вказано, то LOB обрізається до вказаної в `length` довжини у байтах. Інакше LOB повністю очищається.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Класс**OCI-Lob**перейменований на[OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::erase](ocilob.erase.md)
