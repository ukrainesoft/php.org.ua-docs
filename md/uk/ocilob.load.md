---
navigation:
  - ocilob.import.md: '« OCILob::import'
  - ocilob.read.md: 'OCILob::read »'
  - index.md: PHP Manual
  - class.ocilob.md: OCILob
title: 'OCILob::load'
---
# OCILob::load

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

OCILob::load — Повертає вміст об'єкта LOB

### Опис

```methodsynopsis
public OCILob::load(): string|false
```

Повертає вміст LOB. Оскільки виконання скрипта припиниться при перевищенні [memorylimit](ini.core.html#ini.memory-limit)необхідно переконатися, що LOB не перевищує цього обмеження. Тому, в більшості випадків цей метод рекомендується замінювати на [OCILob::read](ocilob.read.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає вміст об'єкта або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Клас **OCI-Lob** перейменований на [OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::read](ocilob.read.md)
