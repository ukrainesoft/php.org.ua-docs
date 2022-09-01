---
navigation:
  - pdostatement.fetchobject.html: '« PDOStatement::fetchObject'
  - pdostatement.getcolumnmeta.html: 'PDOStatement::getColumnMeta »'
  - index.html: PHP Manual
  - class.pdostatement.html: PDOStatement
title: 'PDOStatement::getAttribute'
---
# PDOStatement::getAttribute

(PHP 5> = 5.1.0, PHP 7, PHP 8, PECL pdo> = 0.2.0)

PDOStatement::getAttribute — Отримання атрибуту запиту PDOStatement

### Опис

```methodsynopsis
public PDOStatement::getAttribute(int $name): mixed
```

Отримує значення атрибута запиту. На даний момент не існує загальних атрибутів, є лише характерні для конкретного драйвера:

-   `PDO::ATTR_CURSOR_NAME` (для Firebird та ODBC): Отримання імені курсору для запиту `UPDATE ... WHERE CURRENT OF`

Зверніть увагу, що атрибути драйвера *не повинні* використовуватись з іншими драйверами.

### Список параметрів

`name`

Атрибут для запиту.

### Значення, що повертаються

Повертає значення атрибуту.

### Дивіться також

-   [PDO::getAttribute()](pdo.getattribute.html) - Отримати атрибут з'єднання з базою даних
-   [PDO::setAttribute()](pdo.setattribute.html) - Встановлення атрибуту
-   [PDOStatement::setAttribute()](pdostatement.setattribute.html) - Встановлює атрибут об'єкту PDOStatement
