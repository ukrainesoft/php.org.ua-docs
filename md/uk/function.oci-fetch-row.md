---
navigation:
  - function.oci-fetch-object.html: « ocifetchobject
  - function.oci-fetch.html: ocifetch »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функции
title: ocifetchrow
---
# ocifetchrow

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocifetchrow — Повертає наступний рядок із результату запиту у вигляді нумерованого масиву

### Опис

```methodsynopsis
oci_fetch_row(resource $statement): array|false
```

Повертає нумерований масив, що містить наступний рядок результату запиту. Кожен масив відповідає стовпцю рядка. Ця функція зазвичай викликається в циклі доки не повертає \*\*`false`\*\*якщо в результаті запиту більше немає рядків.

Виклик **ocifetchrow()** аналогічний виклику [ocifetcharray()](function.oci-fetch-array.md) з прапором **`OCI_NUM`** **`OCI_RETURN_NULLS`**

### Список параметрів

`statement`

Коректний ідентифікатор виразу OCI8, отриманий з [ociparse()](function.oci-parse.html) та виконаний функцією [ociexecute()](function.oci-execute.md), або ідентифікатор виразу `REF CURSOR`

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
> Дивіться [ocifetcharray()](function.oci-fetch-array.md) додаткових прикладів результатів запитів.

### Дивіться також

-   [ocifetch()](function.oci-fetch.md) - Вибирає наступний рядок із результату в буфер
-   [ocifetchall()](function.oci-fetch-all.md) - Вибирає всі рядки з результату запиту до двомірного масиву
-   [ocifetcharray()](function.oci-fetch-array.md) - Повертає наступний рядок із результату запиту у вигляді асоціативного чи нумерованого масиву
-   [ocifetchassoc()](function.oci-fetch-assoc.md) - Повертає наступний рядок із результату запиту у вигляді асоціативного масиву
-   [ocifetchobject()](function.oci-fetch-object.md) - Повертає наступний рядок із результату запиту у вигляді об'єкта
