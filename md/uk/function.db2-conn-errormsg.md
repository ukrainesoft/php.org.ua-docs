---
navigation:
  - function.db2-conn-error.md: « db2\_conn\_error
  - function.db2-connect.md: db2\_connect »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_conn\_errormsg
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_conn\_errormsg

(PECL ibm\_db2 >= 1.0.0)

db2\_conn\_errormsg — Повертає останнє повідомлення про помилку підключення та значення SQLCODE

### Опис

```methodsynopsis
db2_conn_errormsg(?resource $connection = null): string
```

Повертає повідомлення про помилку та значення SQLCODE, що є причиною, через яку остання спроба підключення до бази даних завершилася невдачею. Оскільки [db2\_connect()](function.db2-connect.md) повертає **`false`** у разі невдалої спроби підключення, не потрібно передавати жодних параметрів у **db2\_conn\_errormsg()** для отримання відповідного повідомлення про помилку та значення SQLCODE.

Однак, якщо з'єднання було успішним, але згодом стало недійсним, можна передати параметр `connection`, щоб отримати відповідне повідомлення про помилку та значення SQLCODE для конкретного з'єднання.

### Список параметрів

`connection`

Ресурс підключення, пов'язаний із підключенням, яке спочатку було успішним, але згодом стало недійсним.

### Значення, що повертаються

Повертає рядок, що містить повідомлення про помилку та значення SQLCODE, отримане внаслідок невдалої спроби підключення. Якщо при останній спробі помилок не виникло, **db2\_conn\_errormsg()** повертає порожній рядок.

### Приклади

**Приклад #1 Отримання повідомлення про помилку, повернутий у разі невдалої спроби підключення**

У цьому прикладі показано, як повернути повідомлення про помилку та значення SQLCODE після навмисної передачі неприпустимих параметрів [db2\_connect()](function.db2-connect.md)

```php
<?php
$conn = db2_connect('badname', 'baduser', 'badpassword');
if (!$conn) {
    print db2_conn_errormsg();
}
?>
```

Результат виконання наведеного прикладу:

```
[IBM][CLI Driver] SQL1013N  The database alias name
or database name "BADNAME" could not be found.  SQLSTATE=42705
 SQLCODE=-1013
```

### Дивіться також

-   [db2\_conn\_error()](function.db2-conn-error.md) \- Повертає рядок, що містить значення SQLSTATE, повернене останньою спробою підключення
-   [db2\_connect()](function.db2-connect.md) \- Повертає з'єднання з базою даних
-   [db2\_stmt\_error()](function.db2-stmt-error.md) \- Повертає рядок, що містить SQLSTATE, повернутий SQL-оператором
-   [db2\_stmt\_errormsg()](function.db2-stmt-errormsg.md) \- Повертає рядок, що містить останнє повідомлення про помилку SQL-виразу
