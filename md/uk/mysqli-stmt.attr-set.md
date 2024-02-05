---
navigation:
  - mysqli-stmt.attr-get.md: '« mysqli\_stmt::attr\_get'
  - mysqli-stmt.bind-param.md: 'mysqli\_stmt::bind\_param »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::attr\_set'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::attr\_set

# mysqli\_stmt\_attr\_set

(PHP 5, PHP 7, PHP 8)

mysqli\_stmt::attr\_set -- mysqli\_stmt\_attr\_set — Змінює поведінку підготовленого запиту

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

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

`attribute`

Атрибут, що встановлюється. Він може приймати такі значення:

**Значення атрибуту**

| Символ | Опис |
| --- | --- |
| MYSQLI\_STMT\_ATTR\_UPDATE\_MAX\_LENGTH | Якщо дорівнює **`true`**, то[mysqli\_stmt\_store\_result()](mysqli-stmt.store-result.md) оновлює метадані значенням `MYSQL_FIELD->max_length` |
| MYSQLI\_STMT\_ATTR\_CURSOR\_TYPE | Тип вказівника, який потрібно відкрити для запиту під час виклику [mysqli\_stmt\_execute()](mysqli-stmt.execute.md). . `value` може бути `MYSQLI_CURSOR_TYPE_NO_CURSOR`(по умолчанию) или`MYSQLI_CURSOR_TYPE_READ_ONLY` |
| MYSQLI\_STMT\_ATTR\_PREFETCH\_ROWS | Кількість рядків, які потрібно вибрати із сервера під час використання покажчика. . `value` може бути в діапазоні від 1 максимального значення типу unsigned long. За замовчуванням 1. |

Якщо використовується опція `MYSQLI_STMT_ATTR_CURSOR_TYPE`вместе с`MYSQLI_CURSOR_TYPE_READ_ONLY`, то покажчик буде відкритий для запиту, коли буде запущена [mysqli\_stmt\_execute()](mysqli-stmt.execute.md). Якщо вже є відкритий покажчик від попереднього запуску [mysqli\_stmt\_execute()](mysqli-stmt.execute.md), то покажчик буде закрито перед відкриттям нового . [mysqli\_stmt\_reset()](mysqli-stmt.reset.md) також закриває будь-який відкритий покажчик перед підготовкою запиту перед перезапуском . [mysqli\_stmt\_free\_result()](mysqli-stmt.free-result.md) закриває будь-який відкритий покажчик.

Якщо ви відкриваєте вказівник для підготовленого запиту, у використанні [mysqli\_stmt\_store\_result()](mysqli-stmt.store-result.md) немає необхідності.

`value`

Значення, що присвоюється атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### Дивіться також

-   [» Connector/MySQL mysql\_stmt\_attr\_set()](http://dev.mysql.com/doc/en/mysql-stmt-attr-set.md)
