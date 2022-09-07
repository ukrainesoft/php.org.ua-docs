---
navigation:
  - mysqli-stmt.attr-get.md: '« mysqlistmt::attrget'
  - mysqli-stmt.bind-param.md: 'mysqlistmt::bindparam »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqlistmt
title: 'mysqlistmt::attrset'
---
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

Тільки для процедурного стилю: об'єкт [mysqlistmt](class.mysqli-stmt.md), отриманий за допомогою [mysqlistmtinit()](mysqli.stmt-init.md)

`attribute`

Атрибут, що встановлюється. Він може приймати такі значення:

**Значення атрибуту**

| Символ | Описание |
| --- | --- |
| MYSQLISTMTATTRUPDATEMAXLENGTH | Якщо дорівнює **`true`**, то [mysqlistmtstoreresult()](mysqli-stmt.store-result.md) оновлює метадані значенням `MYSQL_FIELD->max_length` |
| MYSQLISTMTATTRCURSORTYPE | Тип вказівника, який потрібно відкрити для запиту під час виклику [mysqlistmtexecute()](mysqli-stmt.execute.md). . `value` може бути `MYSQLI_CURSOR_TYPE_NO_CURSOR` (за замовчуванням) або `MYSQLI_CURSOR_TYPE_READ_ONLY` |
| MYSQLISTMTATTRPREFETCHROWS | Число рядків, які необхідно вибрати з сервера під час використання покажчика . `value` може бути в діапазоні від 1 максимального значення типу unsigned long. За замовчуванням 1. |

Якщо використовується опція `MYSQLI_STMT_ATTR_CURSOR_TYPE` разом з `MYSQLI_CURSOR_TYPE_READ_ONLY`, то покажчик буде відкритий для запиту, коли буде запущена [mysqlistmtexecute()](mysqli-stmt.execute.md). Якщо вже є відкритий покажчик від попереднього запуску [mysqlistmtexecute()](mysqli-stmt.execute.md), то покажчик буде закрито перед відкриттям нового . [mysqlistmtreset()](mysqli-stmt.reset.md) також закриває будь-який відкритий покажчик перед підготовкою запиту перед перезапуском . [mysqlistmtfreeresult()](mysqli-stmt.free-result.md) закриває будь-який відкритий покажчик.

Якщо ви відкриваєте вказівник для підготовленого запиту, у використанні [mysqlistmtstoreresult()](mysqli-stmt.store-result.md) немає необхідності.

`value`

Значення, що присвоюється атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [» Connector/MySQL mysqlstmtattrset()](http://dev.mysql.com/doc/en/mysql-stmt-attr-set.md)
