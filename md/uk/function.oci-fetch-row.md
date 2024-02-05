---
navigation:
  - function.oci-fetch-object.md: « oci\_fetch\_object
  - function.oci-fetch.md: oci\_fetch »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_fetch\_row
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_fetch\_row

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_fetch\_row — Повертає наступний рядок із результату запиту у вигляді нумерованого масиву

### Опис

```methodsynopsis
oci_fetch_row(resource $statement): array|false
```

Повертає нумерований масив, що містить наступний рядок результату запиту. Кожен масив відповідає стовпцю рядка. Ця функція зазвичай викликається в циклі доки не повертає \*\*`false`\*\*якщо в результаті запиту більше немає рядків.

Виклик **oci\_fetch\_row()** аналогічний виклику [oci\_fetch\_array()](function.oci-fetch-array.md) з прапором **`OCI_NUM`** **`OCI_RETURN_NULLS`**

### Список параметрів

`statement`

Коректний ідентифікатор виразу OCI8, отриманий з [oci\_parse()](function.oci-parse.md) та виконаний функцією [oci\_execute()](function.oci-execute.md), або ідентифікатор виразу `REF CURSOR`

### Значення, що повертаються

Повертає нумерований масив. Якщо в `statement` більше немає термін повертає **`false`**

### Приклади

**Приклад #1 Приклад використання** oci\_fetch\_row()\*\*\*\*

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT department_id, department_name FROM departments');
oci_execute($stid);

while (($row = oci_fetch_row($stid)) != false) {
    echo $row[0] . " " . $row[1] . "<br>\n";
}

oci_free_statement($stid);
oci_close($conn);

?>
```

### Примітки

> **Зауваження** :
> 
> Смотрите[oci\_fetch\_array()](function.oci-fetch-array.md) додаткових прикладів результатів запитів.

### Дивіться також

-   [oci\_fetch()](function.oci-fetch.md) \- Вибирає наступний рядок із результату в буфер
-   [oci\_fetch\_all()](function.oci-fetch-all.md) \- Вибирає всі рядки з результату запиту до двомірного масиву
-   [oci\_fetch\_array()](function.oci-fetch-array.md) \- Повертає наступний рядок із результату запиту у вигляді асоціативного чи нумерованого масиву
-   [oci\_fetch\_assoc()](function.oci-fetch-assoc.md) \- Повертає наступний рядок із результату запиту у вигляді асоціативного масиву
-   [oci\_fetch\_object()](function.oci-fetch-object.md) \- Повертає наступний рядок із результату запиту у вигляді об'єкта
