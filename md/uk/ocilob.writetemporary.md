---
navigation:
  - ocilob.write.html: '« OCILob::write'
  - ocilob.writetofile.html: 'OCILob::writeToFile »'
  - index.html: PHP Manual
  - class.ocilob.html: OCILob
title: 'OCILob::writeTemporary'
---
# OCILob::writeTemporary

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

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

-   **`OCI_TEMP_BLOB`** для створення тимчасових BLOB
-   **`OCI_TEMP_CLOB`** для створення тимчасових CLOB

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Клас **OCI-Lob** перейменований на [OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::close](ocilob.close.md)
