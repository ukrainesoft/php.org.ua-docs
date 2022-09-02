---
navigation:
  - ocilob.rewind.md: '« OCILob::rewind'
  - ocilob.savefile.md: 'OCILob::saveFile »'
  - index.md: PHP Manual
  - class.ocilob.md: OCILob
title: 'OCILob::save'
---
# OCILob::save

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

OCILob::save — Зберігає дані в LOB

### Опис

```methodsynopsis
public OCILob::save(string $data, int $offset = 0): bool
```

Зберігає дані з параметра `data` в об'єкт LOB.

### Список параметрів

`data`

Дані для збереження.

`offset`

Може використовуватися для вказівки усунення від початку LOB.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Клас **OCI-Lob** перейменований на [OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::write](ocilob.write.md)
-   [OCILob::import](ocilob.import.md)
