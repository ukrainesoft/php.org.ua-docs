---
navigation:
  - function.oci-fetch-row.html: « ocifetchrow
  - function.oci-field-is-null.html: ocifieldісnull »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функции
title: ocifetch
---
# ocifetch

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocifetch - Вибирає наступний рядок з результату в буфер

### Опис

```methodsynopsis
oci_fetch(resource $statement): bool
```

Вибирає наступний рядок із результату запиту у внутрішній буфер, доступний за допомогою [ociresult()](function.oci-result.html) або через змінні, заздалегідь визначені за допомогою [ocidefineбname()](function.oci-define-by-name.md)

Дивіться [ocifetcharray()](function.oci-fetch-array.md) для більш детальної інформації щодо вибору даних.

### Список параметрів

`statement`

Коректний ідентифікатор виразу OCI8, отриманий з [ociparse()](function.oci-parse.html) та виконаний функцією [ociexecute()](function.oci-execute.md), або ідентифікатор виразу `REF CURSOR`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`**, якщо в результаті `statement` більше немає лав.

### Приклади

**Приклад #1 Приклад використання **ocifetch()** з певними змінними**

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$sql = 'SELECT location_id, city FROM locations WHERE location_id < 1200';
$stid = oci_parse($conn, $sql);

// Определение переменных ДОЛЖНО быть произведено до запуска
oci_define_by_name($stid, 'LOCATION_ID', $locid);
oci_define_by_name($stid, 'CITY', $city);

oci_execute($stid);

// С каждой выборкой переменные заполняются данными следующего ряда
while (oci_fetch($stid)) {
    echo "Идентификатор местоположения $city = $locid<br>\n";
}

// Выведет:
//   Идентификатор местоположения Roma = 1000
//   Идентификатор местоположения Venice = 1100

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #2 Приклад використання **ocifetch()** з [ociresult()](function.oci-result.md)**

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
    echo oci_result($stid, 'LOCATION_ID') . " = ";
    echo oci_result($stid, 'CITY') . "<br>\n";
}

// Выведет:
//   1000 = Roma
//   1100 = Venice

oci_free_statement($stid);
oci_close($conn);

?>
```

### Примітки

> **Зауваження**
> 
> Не повертає рядки для неявних результуючих наборів у Oracle Database. Використовуйте замість цієї функції функцію [ocifetcharray()](function.oci-fetch-array.md)

### Дивіться також

-   [ocidefineбname()](function.oci-define-by-name.md) - зіставляє змінну PHP стовпцю результату запиту
-   [ocifetchall()](function.oci-fetch-all.md) - Вибирає всі рядки з результату запиту до двомірного масиву
-   [ocifetcharray()](function.oci-fetch-array.md) - Повертає наступний рядок із результату запиту у вигляді асоціативного чи нумерованого масиву
-   [ocifetchassoc()](function.oci-fetch-assoc.md) - Повертає наступний рядок із результату запиту у вигляді асоціативного масиву
-   [ocifetchobject()](function.oci-fetch-object.md) - Повертає наступний рядок із результату запиту у вигляді об'єкта
-   [ocifetchrow()](function.oci-fetch-row.md) - Повертає наступний рядок із результату запиту у вигляді нумерованого масиву
-   [ociresult()](function.oci-result.md) - Повертає значення поля із результату запиту
