---
navigation:
  - function.oci-register-taf-callback.md: « oci\_register\_taf\_callback
  - function.oci-rollback.md: oci\_rollback »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_result

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_result — Повертає значення поля з результату запиту

### Опис

```methodsynopsis
oci_result(resource $statement, string|int $column): mixed
```

Повертає дані поля `column` поточного рядка, що повертається функцією [oci\_fetch()](function.oci-fetch.md)

Для отримання детальнішої інформації щодо відображення типів даних модуля OCI8 зверніться до [типів даних, що підтримуються драйвером](oci8.datatypes.md)

### Список параметрів

`statement`

`column`

Може бути задано номером поля (починаючи з 1) або на ім'я. Регістр імені поля повинен бути таким самим, як і у поля, описаного в метаданих Oracle, яке завжди у верхньому регістрі для полів, створених реєстронезалежними.

### Значення, що повертаються

Повертає всі значення у вигляді рядка за винятком абстрактних типів (ROWIDs, LOBs та FILEs). Повертає \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования[oci\_fetch()](function.oci-fetch.md)с**oci\_result()\*\*\*\*

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$sql = 'SELECT location_id, city FROM locations WHERE location_id < 1200';
$stid = oci_parse($conn, $sql);
oci_execute($stid);

while (oci_fetch($stid)) {
    echo oci_result($stid, 'LOCATION_ID') . " - это ";
    echo oci_result($stid, 'CITY') . "<br>\n";
}

// Выведет:
//   1000 - это Roma
//   1100 - это Venice

oci_free_statement($stid);
oci_close($conn);

?>
```

### Дивіться також

-   [oci\_fetch\_array()](function.oci-fetch-array.md) \- Повертає наступний рядок із результату запиту у вигляді асоціативного чи нумерованого масиву
-   [oci\_fetch\_assoc()](function.oci-fetch-assoc.md) \- Повертає наступний рядок із результату запиту у вигляді асоціативного масиву
-   [oci\_fetch\_object()](function.oci-fetch-object.md) \- Повертає наступний рядок із результату запиту у вигляді об'єкта
-   [oci\_fetch\_row()](function.oci-fetch-row.md) \- Повертає наступний рядок із результату запиту у вигляді нумерованого масиву
-   [oci\_fetch\_all()](function.oci-fetch-all.md) \- Вибирає всі рядки з результату запиту до двомірного масиву
