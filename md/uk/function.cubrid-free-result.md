---
navigation:
  - function.cubrid-fetch.md: « cubridfetch
  - function.cubrid-get-autocommit.md: cubridgetautocommit »
  - index.md: PHP Manual
  - ref.cubrid.md: Функции CUBRID
title: cubridfreeresult
---
# cubridfreeresult

(PECL CUBRID >= 8.3.0)

cubridfreeresult — Звільняє пам'ять, зайняту даними результату

### Опис

```methodsynopsis
cubrid_free_result(resource $req_identifier): bool
```

Функція звільняє пам'ять, зайняту даними результату. Вона повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Варто звернути увагу на те, що функція тепер може лише звільняти буфер вибірки клієнта, і якщо необхідно звільнити всю пам'ять, то потрібно використовувати функцію [cubridcloserequest()](function.cubrid-close-request.md)

### Список параметрів

`req_identifier`

Ідентифікатор запиту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridfreeresult()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

$req = cubrid_execute($conn, "SELECT * FROM history WHERE host_year=2004 ORDER BY event_code");
$row = cubrid_fetch_assoc($req);
var_dump($row);

cubrid_free_result($req);
cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

```
array(5) {
  ["event_code"]=>
  string(5) "20005"
  ["athlete"]=>
  string(12) "Hayes Joanna"
  ["host_year"]=>
  string(4) "2004"
  ["score"]=>
  string(5) "12.37"
  ["unit"]=>
  string(4) "time"
}
```
