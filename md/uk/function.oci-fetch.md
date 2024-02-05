---
navigation:
  - function.oci-fetch-row.md: « oci\_fetch\_row
  - function.oci-field-is-null.md: oci\_field\_is\_null »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_fetch
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_fetch

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_fetch - Вибирає наступний рядок з результату в буфер

### Опис

```methodsynopsis
oci_fetch(resource $statement): bool
```

Вибирає наступний рядок із результату запиту у внутрішній буфер, доступний за допомогою [oci\_result()](function.oci-result.md) або через змінні, заздалегідь визначені за допомогою [oci\_define\_by\_name()](function.oci-define-by-name.md)

Смотрите[oci\_fetch\_array()](function.oci-fetch-array.md) для більш детальної інформації щодо вибору даних.

### Список параметрів

`statement`

Коректний ідентифікатор виразу OCI8, отриманий з [oci\_parse()](function.oci-parse.md) та виконаний функцією [oci\_execute()](function.oci-execute.md), або ідентифікатор виразу `REF CURSOR`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`**, если в результате`statement` більше немає лав.

### Приклади

**Пример #1 Пример использования**oci\_fetch()\*\* з певними змінними\*\*

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$sql = 'SELECT location_id, city FROM locations WHERE location_id < 1200';
$stid = oci_parse($conn, $sql);

// Определение переменных ДОЛЖНО быть произведено до запуска
oci_define_by_name($stid, 'LOCATION_ID', $locid);
oci_define_by_name($stid, 'CITY', $city);

oci_execute($stid);

// С каждой выборкой переменные заполняются данными следующего ряда
while (oci_fetch($stid)) {
    echo "Идентификатор местоположения $city = $locid<br>\n";
}

// Выведет:
//   Идентификатор местоположения Roma = 1000
//   Идентификатор местоположения Venice = 1100

oci_free_statement($stid);
oci_close($conn);

?>
```

**Пример #2 Пример использования**oci\_fetch()**с[oci\_result()](function.oci-result.md)**

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
    echo oci_result($stid, 'LOCATION_ID') . " = ";
    echo oci_result($stid, 'CITY') . "<br>\n";
}

// Выведет:
//   1000 = Roma
//   1100 = Venice

oci_free_statement($stid);
oci_close($conn);

?>
```

### Примітки

> **Зауваження** :
> 
> Не повертає рядки для неявних результуючих наборів у Oracle Database. Використовуйте замість цієї функції функцію [oci\_fetch\_array()](function.oci-fetch-array.md)

### Дивіться також

-   [oci\_define\_by\_name()](function.oci-define-by-name.md) \- зіставляє змінну PHP стовпцю результату запиту
-   [oci\_fetch\_all()](function.oci-fetch-all.md) \- Вибирає всі рядки з результату запиту до двомірного масиву
-   [oci\_fetch\_array()](function.oci-fetch-array.md) \- Повертає наступний рядок із результату запиту у вигляді асоціативного чи нумерованого масиву
-   [oci\_fetch\_assoc()](function.oci-fetch-assoc.md) \- Повертає наступний рядок із результату запиту у вигляді асоціативного масиву
-   [oci\_fetch\_object()](function.oci-fetch-object.md) \- Повертає наступний рядок із результату запиту у вигляді об'єкта
-   [oci\_fetch\_row()](function.oci-fetch-row.md) \- Повертає наступний рядок із результату запиту у вигляді нумерованого масиву
-   [oci\_result()](function.oci-result.md) \- Повертає значення поля із результату запиту
