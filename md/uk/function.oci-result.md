---
navigation:
  - function.oci-register-taf-callback.html: « ociregistertafcallback
  - function.oci-rollback.html: ocirollback »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функции
title: ociresult
---
# ociresult

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ociresult — Повертає значення поля з результату запиту

### Опис

```methodsynopsis
oci_result(resource $statement, string|int $column): mixed
```

Повертає дані поля `column` поточного рядка, що повертається функцією [ocifetch()](function.oci-fetch.md)

За подробицями щодо відображення типів даних, що здійснюється модулем OCI8, зверніться до [типів даних, що підтримуються драйвером](oci8.datatypes.md)

### Список параметрів

`statement`

`column`

Може бути задано номером поля (починаючи з 1) або на ім'я. Регістр імені поля повинен бути таким самим, як і у поля, описаного в метаданих Oracle, яке завжди у верхньому регістрі для полів, створених реєстронезалежними.

### Значення, що повертаються

Повертає всі значення у вигляді рядка за винятком абстрактних типів (ROWIDs, LOBs та FILEs). Повертає **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання [ocifetch()](function.oci-fetch.md) з **ociresult()****

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$sql = 'SELECT location_id, city FROM locations WHERE location_id < 1200';
$stid = oci_parse($conn, $sql);
oci_execute($stid);

while (oci_fetch($stid)) {
    echo oci_result($stid, 'LOCATION_ID') . " - это ";
    echo oci_result($stid, 'CITY') . "<br>\n";
}

// Выведет:
//   1000 - это Roma
//   1100 - это Venice

oci_free_statement($stid);
oci_close($conn);

?>
```

### Примітки

> **Зауваження**
> 
> У версіях PHP нижче 5.0.0 ця функція називалася [ociresult()](function.ociresult.md). У PHP 5.0.0 і вище [ociresult()](function.ociresult.md) є аліасом **ociresult()** з метою зворотної сумісності. Ви можете продовжувати використовувати це ім'я, але це не рекомендується.

### Дивіться також

-   [ocifetcharray()](function.oci-fetch-array.md) - Повертає наступний рядок із результату запиту у вигляді асоціативного чи нумерованого масиву
-   [ocifetchassoc()](function.oci-fetch-assoc.md) - Повертає наступний рядок із результату запиту у вигляді асоціативного масиву
-   [ocifetchobject()](function.oci-fetch-object.md) - Повертає наступний рядок із результату запиту у вигляді об'єкта
-   [ocifetchrow()](function.oci-fetch-row.md) - Повертає наступний рядок із результату запиту у вигляді нумерованого масиву
-   [ocifetchall()](function.oci-fetch-all.md) - Вибирає всі рядки з результату запиту до двомірного масиву
