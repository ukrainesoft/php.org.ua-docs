---
navigation:
  - ocilob.append.md: '« OCILob::append'
  - ocilob.eof.md: 'OCILob::eof »'
  - index.md: PHP Manual
  - class.ocilob.md: OCILob
title: 'OCILob::close'
---
# OCILob::close

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

OCILob::close — Закриває дескриптор об'єкта LOB

### Опис

```methodsynopsis
public OCILob::close(): bool
```

Закриває дескриптор об'єкта LOB чи FILE. Функцію слід використовувати лише разом із [OCILob::writeTemporary](ocilob.writetemporary.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Клас **OCI-Lob** перейменований на [OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::writeTemporary](ocilob.writetemporary.md)
