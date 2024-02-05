---
navigation:
  - function.oci-fetch-array.md: « oci\_fetch\_array
  - function.oci-fetch-object.md: oci\_fetch\_object »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_fetch\_assoc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_fetch\_assoc

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_fetch\_assoc — Повертає наступний рядок із результату запиту у вигляді асоціативного масиву

### Опис

```methodsynopsis
oci_fetch_assoc(resource $statement): array|false
```

Повертає асоціативний масив, що містить наступний рядок результату виконання запиту. Кожен елемент масиву відповідає стовпцю поточного рядка. Ця функція зазвичай викликається в циклі, доки не повертає \*\*`false`\*\*якщо більше немає рядків.

Результат виконання **oci\_fetch\_assoc()** ідентичний до виконання [oci\_fetch\_array()](function.oci-fetch-array.md) з прапором **`OCI_ASSOC`** **`OCI_RETURN_NULLS`**

### Список параметрів

`statement`

Коректний ідентифікатор виразу OCI8, отриманий з [oci\_parse()](function.oci-parse.md) та виконаний функцією [oci\_execute()](function.oci-execute.md), або ідентифікатор виразу `REF CURSOR`

### Значення, що повертаються

Повертає асоціативний масив. Якщо результат запиту рядків більше немає, повертає **`false`**

### Приклади

**Приклад #1 Приклад використання** oci\_fetch\_assoc()\*\*\*\*

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT department_id, department_name FROM departments');
oci_execute($stid);

while (($row = oci_fetch_assoc($stid)) != false) {
    echo $row['DEPARTMENT_ID'] . " " . $row['DEPARTMENT_NAME'] . "<br>\n";
}

oci_free_statement($stid);
oci_close($conn);

?>
```

### Примітки

> **Зауваження** :
> 
> Дивіться додаткові приклади отримання рядків у [oci\_fetch\_array()](function.oci-fetch-array.md)

### Дивіться також

-   [oci\_fetch()](function.oci-fetch.md) \- Вибирає наступний рядок із результату в буфер
-   [oci\_fetch\_all()](function.oci-fetch-all.md) \- Вибирає всі рядки з результату запиту до двомірного масиву
-   [oci\_fetch\_array()](function.oci-fetch-array.md) \- Повертає наступний рядок із результату запиту у вигляді асоціативного чи нумерованого масиву
-   [oci\_fetch\_object()](function.oci-fetch-object.md) \- Повертає наступний рядок із результату запиту у вигляді об'єкта
-   [oci\_fetch\_row()](function.oci-fetch-row.md) \- Повертає наступний рядок із результату запиту у вигляді нумерованого масиву
