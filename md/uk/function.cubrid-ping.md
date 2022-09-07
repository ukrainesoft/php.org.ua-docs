---
navigation:
  - function.cubrid-num-fields.md: « cubridnumfields
  - function.cubrid-query.md: cubridquery »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubridping
---
# cubridping

(PECL CUBRID >= 8.3.1)

cubridping — Перевіряє, чи живе з'єднання до сервера і перепідключає його, якщо ні

### Опис

```methodsynopsis
cubrid_ping(resource $conn_identifier = ?): bool
```

Перевіряє, чи живе з'єднання з сервером.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання. Якщо не встановлено, то буде використано останнє відкрите за допомогою [cubridconnect()](function.cubrid-connect.md) з'єднання.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо з'єднання працює, інакше **`false`**

### Приклади

**Приклад #1 Приклад використання **cubridping()****

```php
<?php
set_time_limit(0);

$conn = cubrid_connect('localhost', 33000, 'demodb');

/* Предположим, что это ну очень длинный запрос */
$sql = "select * from athlete";
$result = cubrid_query($sql);
if (!$result) {
    echo 'Запрос #1 завершился с ошибкой, выходим.';
    exit;
}

/* Проверяем, живо ли ещё соединение и пересоздаем его, если нет */
if (!cubrid_ping($conn)) {
    echo 'Потеряно соединение, выходим после запроса #1';
    exit;
}
cubrid_free_result($result);

/* Так так, соединение работает. Тогда ещё один запрос! */
$sql2 = "select * from code";
$result2 = cubrid_query($sql2);
?>
```
