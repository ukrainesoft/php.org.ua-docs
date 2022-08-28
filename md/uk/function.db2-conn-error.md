Повертає рядок, що містить значення SQLSTATE, повернене останньою спробою підключення

-   [« db2\_commit](function.db2-commit.html)
    
-   [db2\_conn\_errormsg »](function.db2-conn-errormsg.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IBM DB2](ref.ibm-db2.html)
    
-   Повертає рядок, що містить значення SQLSTATE, повернене останньою спробою підключення
    

# db2connerror

(PECL ibmdb2> = 1.0.0)

db2connerror — Повертає рядок, який містить значення SQLSTATE, повернене останньою спробою підключення

### Опис

```methodsynopsis
db2_conn_error(resource $connection = ?): string
```

Повертає значення SQLSTATE, що становить причину, через яку остання спроба підключення до бази даних завершилася невдачею. Оскільки [db2\_connect()](function.db2-connect.html) повертає **`false`** у разі невдалої спроби підключення, не потрібно передавати жодних параметрів у **db2connerror()** для отримання SQLSTATE.

Однак, якщо з'єднання було успішним, але згодом стало недійсним, можна передати параметр `connection`, щоб отримати значення SQLSTATE для конкретного з'єднання.

Щоб дізнатися, що означає SQLSTATE, можна ввести наступну команду в командному рядку DB2 Command Line Processor: **``db2 '? `sqlstate-value`'``**. Також можна викликати [db2\_conn\_errormsg()](function.db2-conn-errormsg.html), щоб отримати явне повідомлення про помилку та відповідне значення SQLCODE.

### Список параметрів

`connection`

Ресурс підключення, пов'язаний із підключенням, яке спочатку було успішним, але згодом стало недійсним.

### Значення, що повертаються

Повертає значення SQLSTATE, отримане внаслідок невдалої спроби підключення. Повертає порожній рядок, якщо під час останньої спроби з'єднання помилок не виникло.

### Приклади

**Приклад #1 Отримання SQLSTATE для невдалої спроби підключення**

У цьому прикладі показано, як повернути значення SQLSTATE після навмисної передачі неприпустимих параметрів [db2\_connect()](function.db2-connect.html)

```php
<?php
$conn = db2_connect('badname', 'baduser', 'badpassword');
if (!$conn) {
    print "SQLSTATE value: " . db2_conn_error();
}
?>
```

Результат виконання цього прикладу:

```
SQLSTATE value: 08001
```

### Дивіться також

-   [db2\_conn\_errormsg()](function.db2-conn-errormsg.html) - Повертає останнє повідомлення про помилку підключення та значення SQLCODE
-   [db2\_connect()](function.db2-connect.html) - Повертає з'єднання з базою даних
-   [db2\_stmt\_error()](function.db2-stmt-error.html) - Повертає рядок, що містить SQLSTATE, повернутий SQL-оператором
-   [db2\_stmt\_errormsg()](function.db2-stmt-errormsg.html) - Повертає рядок, що містить останнє повідомлення про помилку SQL-виразу