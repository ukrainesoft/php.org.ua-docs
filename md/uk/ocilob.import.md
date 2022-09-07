---
navigation:
  - ocilob.getbuffering.md: '« OCILob::getBuffering'
  - ocilob.load.md: 'OCILob::load »'
  - index.md: PHP Manual
  - class.ocilob.md: OCILob
title: 'OCILob::import'
---
# OCILob::import

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

OCILob::import — записує вміст файлу в об'єкт LOB

### Опис

```methodsynopsis
public OCILob::import(string $filename): bool
```

Записує вміст файлу `filename` у поточну позицію об'єкта LOB.

### Список параметрів

`filename`

Шлях до файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Клас **OCI-Lob** перейменований на [OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::export](ocilob.export.md)
-   [OCILob::write](ocilob.write.md)
