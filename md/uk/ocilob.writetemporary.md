---
navigation:
  - ocilob.write.md: '« OCILob::write'
  - ocilob.writetofile.md: 'OCILob::writeToFile »'
  - index.md: PHP Manual
  - class.ocilob.md: OCILob
title: 'OCILob::writeTemporary'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OCILob::writeTemporary

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

OCILob::writeTemporary — Записує великий тимчасовий об'єкт (LOB)

### Опис

```methodsynopsis
public OCILob::writeTemporary(string $data, int $type = OCI_TEMP_CLOB): bool
```

Створює великий тимчасовий об'єкт і записує в нього дані `data`

Після завершення роботи з цим об'єктом його бажано закрити функцією [OCILob::close](ocilob.close.md)

### Список параметрів

`data`

Дані для запису.

`type`

Один з таких варіантів:

-   \*\*`OCI_TEMP_BLOB`\*\*для створення тимчасових BLOB
-   \*\*`OCI_TEMP_CLOB`\*\*для створення тимчасових CLOB

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Класс**OCI-Lob**перейменований на[OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::close](ocilob.close.md)
