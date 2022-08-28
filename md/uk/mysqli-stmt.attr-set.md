Змінює поведінку підготовленого запиту

-   [« mysqli\_stmt::attr\_get](mysqli-stmt.attr-get.html)
    
-   [mysqli\_stmt::bind\_param »](mysqli-stmt.bind-param.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli\_stmt](class.mysqli-stmt.html)
    
-   Змінює поведінку підготовленого запиту
    

# mysqlistmt::attrset

# mysqlistmtattrset

(PHP 5, PHP 7, PHP 8)

mysqlistmt::attrset - mysqlistmtattrset — Змінює поведінку підготовленого запиту

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::attr_set(int $attribute, int $value): bool
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_attr_set(mysqli_stmt $statement, int $attribute, int $value): bool
```

Використовується для зміни поведінки підготовленого запиту. Ця функція може бути викликана кілька разів для встановлення кількох атрибутів.

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.html), отриманий за допомогою [mysqli\_stmt\_init()](mysqli.stmt-init.html)

`attribute`

Атрибут, що встановлюється. Він може приймати такі значення:

**Значення атрибуту**

| Символ                        | Описание                                                                                                                                                                                                                        |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MYSQLISTMTATTRUPDATEMAXLENGTH | Якщо дорівнює **`true`**, то [mysqli\_stmt\_store\_result()](mysqli-stmt.store-result.html) оновлює метадані значенням `MYSQL_FIELD->max_length`                                                                                |
| MYSQLISTMTATTRCURSORTYPE      | Тип вказівника, який потрібно відкрити для запиту під час виклику [mysqli\_stmt\_execute()](mysqli-stmt.execute.html). . `value` може бути `MYSQLI_CURSOR_TYPE_NO_CURSOR` (за замовчуванням) або `MYSQLI_CURSOR_TYPE_READ_ONLY` |
| MYSQLISTMTATTRPREFETCHROWS    | Число рядків, які необхідно вибрати з сервера під час використання покажчика . `value` може бути в діапазоні від 1 максимального значення типу unsigned long. За замовчуванням 1.                                               |

Якщо використовується опція `MYSQLI_STMT_ATTR_CURSOR_TYPE` разом з `MYSQLI_CURSOR_TYPE_READ_ONLY`, то покажчик буде відкритий для запиту, коли буде запущена [mysqli\_stmt\_execute()](mysqli-stmt.execute.html). Якщо вже є відкритий покажчик від попереднього запуску [mysqli\_stmt\_execute()](mysqli-stmt.execute.html), то покажчик буде закрито перед відкриттям нового . [mysqli\_stmt\_reset()](mysqli-stmt.reset.html) також закриває будь-який відкритий покажчик перед підготовкою запиту перед перезапуском . [mysqli\_stmt\_free\_result()](mysqli-stmt.free-result.html) закриває будь-який відкритий покажчик.

Якщо ви відкриваєте вказівник для підготовленого запиту, у використанні [mysqli\_stmt\_store\_result()](mysqli-stmt.store-result.html) немає необхідності.

`value`

Значення, що присвоюється атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [» Connector/MySQL mysql\_stmt\_attr\_set()](http://dev.mysql.com/doc/en/mysql-stmt-attr-set.html)