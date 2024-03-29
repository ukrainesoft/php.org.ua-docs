---
navigation:
  - pdostatement.rowcount.md: '« PDOStatement::rowCount'
  - pdostatement.setfetchmode.md: 'PDOStatement::setFetchMode »'
  - index.md: PHP Manual
  - class.pdostatement.md: PDOStatement
title: 'PDOStatement::setAttribute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDOStatement::setAttribute

(PHP 5 >= 5.1.0, PHP 7, PHP 8, PECL pdo >= 0.2.0)

PDOStatement::setAttribute — Встановлює атрибут об'єкту PDOStatement

### Опис

```methodsynopsis
public PDOStatement::setAttribute(int $attribute, mixed $value): bool
```

Задає атрибут об'єкта PDOStatement. На даний момент жодних загальних атрибутів встановлювати не можна, лише характерні для конкретного драйвера:

-   `PDO::ATTR_CURSOR_NAME`(для Firebird та ODBC): Вказує ім'я курсора для запитів виду`UPDATE ... WHERE CURRENT OF`

Зверніть увагу, що атрибути драйвера *не повинні* використовуватись з іншими драйверами.

### Список параметрів

`attribute`

Атрибут зміни.

`value`

Значение для установки параметра`attribute` може вимагати певного типу, залежно від атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [PDO::getAttribute()](pdo.getattribute.md) \- Отримує атрибут з'єднання з базою даних
-   [PDO::setAttribute()](pdo.setattribute.md) \- Встановлення атрибуту
-   [PDOStatement::getAttribute()](pdostatement.getattribute.md) \- Отримання значення атрибуту запиту PDOStatement
