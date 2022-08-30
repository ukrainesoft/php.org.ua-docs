Повертає наступний рядок із результату запиту у вигляді асоціативного масиву

-   [« ocifetcharray](function.oci-fetch-array.html)
    
-   [ocifetchobject »](function.oci-fetch-object.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8 Функции](ref.oci8.html)
    
-   Повертає наступний рядок із результату запиту у вигляді асоціативного масиву
    

# ocifetchassoc

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocifetchassoc — Повертає наступний рядок із результату запиту у вигляді асоціативного масиву

### Опис

```methodsynopsis
oci_fetch_assoc(resource $statement): array|false
```

Повертає асоціативний масив, що містить наступний рядок результату виконання запиту. Кожен елемент масиву відповідає стовпцю поточного рядка. Ця функція зазвичай викликається в циклі, доки не повертає \*\*`false`\*\*якщо більше немає рядків.

Результат виконання **ocifetchassoc()** ідентичний до виконання [ocifetcharray()](function.oci-fetch-array.html) з прапором **`OCI_ASSOC`** **`OCI_RETURN_NULLS`**

### Список параметрів

`statement`

Коректний ідентифікатор виразу OCI8, отриманий з [ociparse()](function.oci-parse.html) та виконаний функцією [ociexecute()](function.oci-execute.html), або ідентифікатор виразу `REF CURSOR`

### Значення, що повертаються

Повертає асоціативний масив. Якщо результат запиту рядків більше немає, повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **ocifetchassoc()****

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT department_id, department_name FROM departments');
oci_execute($stid);

while (($row = oci_fetch_assoc($stid)) != false) {
    echo $row['DEPARTMENT_ID'] . " " . $row['DEPARTMENT_NAME'] . "<br>\n";
}

oci_free_statement($stid);
oci_close($conn);

?>
```

### Примітки

> **Зауваження**
> 
> Дивіться додаткові приклади отримання рядків у [ocifetcharray()](function.oci-fetch-array.html)

### Дивіться також

-   [ocifetch()](function.oci-fetch.html) - Вибирає наступний рядок із результату в буфер
-   [ocifetchall()](function.oci-fetch-all.html) - Вибирає всі рядки з результату запиту до двомірного масиву
-   [ocifetcharray()](function.oci-fetch-array.html) - Повертає наступний рядок із результату запиту у вигляді асоціативного чи нумерованого масиву
-   [ocifetchobject()](function.oci-fetch-object.html) - Повертає наступний рядок із результату запиту у вигляді об'єкта
-   [ocifetchrow()](function.oci-fetch-row.html) - Повертає наступний рядок із результату запиту у вигляді нумерованого масиву