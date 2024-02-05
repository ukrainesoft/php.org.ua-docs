---
navigation:
  - function.cubrid-fetch.md: « cubrid\_fetch
  - function.cubrid-get-autocommit.md: cubrid\_get\_autocommit »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_free\_result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_free\_result

(PECL CUBRID >= 8.3.0)

cubrid\_free\_result — Звільняє пам'ять, зайняту даними результату

### Опис

```methodsynopsis
cubrid_free_result(resource $req_identifier): bool
```

Функція звільняє пам'ять, зайняту даними результату. Вона повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Варто звернути увагу на те, що функція тепер може лише звільняти буфер вибірки клієнта, і якщо необхідно звільнити всю пам'ять, то потрібно використовувати функцію [cubrid\_close\_request()](function.cubrid-close-request.md)

### Список параметрів

`req_identifier`

Ідентифікатор запиту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**cubrid\_free\_result()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

$req = cubrid_execute($conn, "SELECT * FROM history WHERE host_year=2004 ORDER BY event_code");
$row = cubrid_fetch_assoc($req);
var_dump($row);

cubrid_free_result($req);
cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

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
