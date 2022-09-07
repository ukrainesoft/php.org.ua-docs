---
navigation:
  - function.db2-commit.md: « db2commit
  - function.db2-conn-errormsg.md: db2connerrormsg »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2connerror
---
# db2connerror

(PECL ibmdb2> = 1.0.0)

db2connerror — Повертає рядок, який містить значення SQLSTATE, повернене останньою спробою підключення

### Опис

```methodsynopsis
db2_conn_error(resource $connection = ?): string
```

Повертає значення SQLSTATE, що становить причину, через яку остання спроба підключення до бази даних завершилася невдачею. Оскільки [db2connect()](function.db2-connect.md) повертає **`false`** у разі невдалої спроби підключення, не потрібно передавати жодних параметрів у **db2connerror()** для отримання SQLSTATE.

Однак, якщо з'єднання було успішним, але згодом стало недійсним, можна передати параметр `connection`, щоб отримати значення SQLSTATE для конкретного з'єднання.

Щоб дізнатися, що означає SQLSTATE, можна ввести наступну команду в командному рядку DB2 Command Line Processor: **``db2 '? `sqlstate-value`'``**. Також можна викликати [db2connerrormsg()](function.db2-conn-errormsg.md), щоб отримати явне повідомлення про помилку та відповідне значення SQLCODE.

### Список параметрів

`connection`

Ресурс підключення, пов'язаний із підключенням, яке спочатку було успішним, але згодом стало недійсним.

### Значення, що повертаються

Повертає значення SQLSTATE, отримане внаслідок невдалої спроби підключення. Повертає порожній рядок, якщо під час останньої спроби з'єднання помилок не виникло.

### Приклади

**Приклад #1 Отримання SQLSTATE для невдалої спроби підключення**

У цьому прикладі показано, як повернути значення SQLSTATE після навмисної передачі неприпустимих параметрів [db2connect()](function.db2-connect.md)

```php
<?php
$conn = db2_connect('badname', 'baduser', 'badpassword');
if (!$conn) {
    print "SQLSTATE value: " . db2_conn_error();
}
?>
```

Результат виконання цього прикладу:

```
SQLSTATE value: 08001
```

### Дивіться також

-   [db2connerrormsg()](function.db2-conn-errormsg.md) - Повертає останнє повідомлення про помилку підключення та значення SQLCODE
-   [db2connect()](function.db2-connect.md) - Повертає з'єднання з базою даних
-   [db2stmterror()](function.db2-stmt-error.md) - Повертає рядок, що містить SQLSTATE, повернутий SQL-оператором
-   [db2stmterrormsg()](function.db2-stmt-errormsg.md) - Повертає рядок, що містить останнє повідомлення про помилку SQL-виразу
