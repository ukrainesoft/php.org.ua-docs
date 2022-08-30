Виконує підготовлений SQL-оператор

-   [« cubriderrormsg](function.cubrid-error-msg.html)
    
-   [cubridfetch »](function.cubrid-fetch.html)
    
-   [PHP Manual](index.md)
    
-   [Функции CUBRID](ref.cubrid.md)
    
-   Виконує підготовлений SQL-оператор
    

# cubridexecute

(PECL CUBRID >= 8.3.0)

cubridexecute - Виконує підготовлений SQL-оператор

### Опис

```methodsynopsis
cubrid_execute(resource $conn_identifier, string $sql, int $option = 0): resource
```

```methodsynopsis
cubrid_execute(resource $request_identifier, int $option = 0): bool
```

Функція **cubridexecute()** використовується для виконання цього SQL-оператора. Вона виконує запит, використовуючи `conn_identifier` та SQL, а потім повертає створений ідентифікатор запиту. Функція використовується для простого виконання запиту, коли не потрібно. Крім того, функція **cubridexecute()** використовується для виконання підготовленого оператора за допомогою [cubridprepare()](function.cubrid-prepare.html) і [cubridbind()](function.cubrid-bind.html). У цей час вам необхідно вказати аргументи `request_identifier` і `option`

Параметр `option` використовується для визначення, чи слід отримувати OID після виконання запиту та чи слід виконувати запит у синхронному або асинхронному режимі. Константа **`CUBRID_INCLUDE_OID`** і **`CUBRID_ASYNC`** (або \*\*`CUBRID_EXEC_QUERY_ALL`\*\*Якщо необхідно виконати кілька SQL-операторів) можна вказати за допомогою побітового оператора АБО. Якщо не вказано, жодного з них не вибрано. Якщо встановлено прапор **`CUBRID_EXEC_QUERY_ALL`**, для отримання результатів запиту використовується синхронний режим (syncmode) і в таких випадках застосовуються такі правила:

-   Значення, що повертається - результат першого запиту.
-   Якщо у будь-якому запиті виникає помилка, виконання обробляється як збій.
-   У запиті, що складається з q1 q2 q3, якщо помилка виникає q2 після успішного виконання q1, результат q1 залишається дійсним. Тобто попереднє успішне виконання запиту не відкочується у разі помилки.
-   У разі успішного виконання запиту, результат другого запиту можна отримати за допомогою [cubridnextresult()](function.cubrid-next-result.html)

Якщо першим аргументом є `request_identifier` для виконання функції [cubridprepare()](function.cubrid-prepare.html) можна вказати тільки **`CUBRID_ASYNC`**

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`sql`

SQL для виконання.

`option`

Варіант виконання запиту: **`CUBRID_INCLUDE_OID`** **`CUBRID_ASYNC`** **`CUBRID_EXEC_QUERY_ALL`**

`request_identifier`

Ідентифікатор [cubridprepare()](function.cubrid-prepare.html)

### Значення, що повертаються

Ідентифікатор запиту у разі успішного виконання запиту і якщо першим параметром є connidentifier; **`true`**, у разі успішного виконання запиту та першим аргументом requestidentifier або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Додано новий параметр **`CUBRID_EXEC_QUERY_ALL`** |

### Приклади

**Приклад #1 Приклад використання **cubridexecute()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

$result = cubrid_execute($conn, "SELECT code FROM event WHERE name='100m Butterfly' and gender='M'", CUBRID_ASYNC);
$row = cubrid_fetch_array($result, CUBRID_ASSOC);
$event_code = $row["code"];

cubrid_close_request($result);

$history_req = cubrid_prepare($conn, "SELECT * FROM history WHERE event_code=?");
cubrid_bind($history_req, 1, $event_code, "number");
cubrid_execute($history_req);

printf("%-20s %-9s %-10s %-5s\n", "athlete", "host_year", "score", "unit");
while ($row = cubrid_fetch_array($history_req, CUBRID_ASSOC)) {
    printf("%-20s %-9s %-10s %-5s\n",
        $row["athlete"], $row["host_year"], $row["score"], $row["unit"]);
}

cubrid_close_request($history_req);

cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

```
athlete              host_year score      unit
Phelps Michael       2004      51.25      time
```

### Дивіться також

-   [cubridprepare()](function.cubrid-prepare.html) - Підготовляє SQL-вираз до виконання
-   [cubridbind()](function.cubrid-bind.html) - пов'язує змінні з підготовленим запитом
-   [cubridnextresult()](function.cubrid-next-result.html) - Отримує результат наступного запиту під час виконання кількох SQL-операторів
-   [cubridcloserequest()](function.cubrid-close-request.html) - Закриває обробник запиту
-   [cubridcommit()](function.cubrid-commit.html) - підтвердження транзакції
-   [cubridrollback()](function.cubrid-rollback.html) - Відкат транзакції