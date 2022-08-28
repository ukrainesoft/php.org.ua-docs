Встановлює атрибут об'єкту PDOStatement

-   [« PDOStatement::rowCount](pdostatement.rowcount.html)
    
-   [PDOStatement::setFetchMode »](pdostatement.setfetchmode.html)
    
-   [PHP Manual](index.html)
    
-   [PDOStatement](class.pdostatement.html)
    
-   Встановлює атрибут об'єкту PDOStatement
    

# PDOStatement::setAttribute

(PHP 5> = 5.1.0, PHP 7, PHP 8, PECL pdo> = 0.2.0)

PDOStatement::setAttribute — Встановлює атрибут об'єкту PDOStatement

### Опис

```methodsynopsis
public PDOStatement::setAttribute(int $attribute, mixed $value): bool
```

Задає атрибут об'єкта PDOStatement. На даний момент жодних загальних атрибутів встановлювати не можна, лише характерні для конкретного драйвера:

-   `PDO::ATTR_CURSOR_NAME` (для Firebird та ODBC): Вказує ім'я курсора для запитів виду `UPDATE ... WHERE CURRENT OF`

Зверніть увагу, що атрибути драйвера *не повинні* використовуватись з іншими драйверами.

### Список параметрів

`attribute`

Атрибут зміни.

`value`

Значення для встановлення параметра `attribute` може вимагати певного типу, залежно від атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [PDO::getAttribute()](pdo.getattribute.html) - Отримати атрибут з'єднання з базою даних
-   [PDO::setAttribute()](pdo.setattribute.html) - Встановлення атрибуту
-   [PDOStatement::getAttribute()](pdostatement.getattribute.html) - Отримання значення атрибуту запиту PDOStatement