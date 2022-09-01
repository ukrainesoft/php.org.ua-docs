---
navigation:
  - ocilob.free.md: '« OCILob::free'
  - ocilob.import.md: 'OCILob::import »'
  - index.md: PHP Manual
  - class.ocilob.md: OCILob
title: 'OCILob::getBuffering'
---
# OCILob::getBuffering

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

OCILob::getBuffering — Повертає поточний стан буферизації великого об'єкта (LOB)

### Опис

```methodsynopsis
public OCILob::getBuffering(): bool
```

Повідомляє, чи увімкнена буферизація для великого об'єкта (LOB).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`false`**, якщо буферизація вимкнена, та **`true`**, якщо увімкнено.

### список змін

| Версия | Описание |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Клас **OCI-Lob** перейменований на [OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::setBuffering](ocilob.setbuffering.md)
