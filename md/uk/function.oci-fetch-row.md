Повертає наступний рядок із результату запиту у вигляді нумерованого масиву

-   [« oci\_fetch\_object](function.oci-fetch-object.html)
    
-   [oci\_fetch »](function.oci-fetch.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8 Функции](ref.oci8.html)
    
-   Повертає наступний рядок із результату запиту у вигляді нумерованого масиву
    

# ocifetchrow

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocifetchrow — Повертає наступний рядок із результату запиту у вигляді нумерованого масиву

### Опис

```methodsynopsis
oci_fetch_row(resource $statement): array|false
```

Повертає нумерований масив, що містить наступний рядок результату запиту. Кожен масив відповідає стовпцю рядка. Ця функція зазвичай викликається в циклі доки не повертає **`false`**якщо в результаті запиту більше немає рядків.

Виклик **ocifetchrow()** аналогічний виклику [oci\_fetch\_array()](function.oci-fetch-array.html) з прапором **`OCI_NUM`** **`OCI_RETURN_NULLS`**

### Список параметрів

`statement`

Коректний ідентифікатор виразу OCI8, отриманий з [oci\_parse()](function.oci-parse.html) та виконаний функцією [oci\_execute()](function.oci-execute.html), або ідентифікатор виразу `REF CURSOR`

### Значення, що повертаються

Повертає нумерований масив. Якщо в `statement` більше немає термін повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **ocifetchrow()****

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT department_id, department_name FROM departments');
oci_execute($stid);

while (($row = oci_fetch_row($stid)) != false) {
    echo $row[0] . " " . $row[1] . "<br>\n";
}

oci_free_statement($stid);
oci_close($conn);

?>
```

### Примітки

> **Зауваження**
> 
> Дивіться [oci\_fetch\_array()](function.oci-fetch-array.html) додаткових прикладів результатів запитів.

### Дивіться також

-   [oci\_fetch()](function.oci-fetch.html) - Вибирає наступний рядок із результату в буфер
-   [oci\_fetch\_all()](function.oci-fetch-all.html) - Вибирає всі рядки з результату запиту до двомірного масиву
-   [oci\_fetch\_array()](function.oci-fetch-array.html) - Повертає наступний рядок із результату запиту у вигляді асоціативного чи нумерованого масиву
-   [oci\_fetch\_assoc()](function.oci-fetch-assoc.html) - Повертає наступний рядок із результату запиту у вигляді асоціативного масиву
-   [oci\_fetch\_object()](function.oci-fetch-object.html) - Повертає наступний рядок із результату запиту у вигляді об'єкта