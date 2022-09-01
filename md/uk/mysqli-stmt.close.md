---
navigation:
  - mysqli-stmt.bind-result.html: '« mysqlistmt::bindresult'
  - mysqli-stmt.construct.html: 'mysqlistmt::construct »'
  - index.html: PHP Manual
  - class.mysqli-stmt.html: mysqlistmt
title: 'mysqlistmt::close'
---
# mysqlistmt::close

# mysqlistmtclose

(PHP 5, PHP 7, PHP 8)

mysqlistmt::close -- mysqlistmtclose — Закриває підготовлений запит

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::close(): bool
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_close(mysqli_stmt $statement): bool
```

Закриває підготовлений запит . **mysqlistmtclose()** також звільняє дескриптор запиту. Якщо за поточним запитом отримано результат, ця функція очищає його для того, щоб міг бути виконаний наступний запит.

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqlistmt](class.mysqli-stmt.html), отриманий за допомогою [mysqlistmtinit()](mysqli.stmt-init.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [mysqliprepare()](mysqli.prepare.html) - готує SQL вираз до виконання
