---
navigation:
  - function.cubrid-close-prepare.md: « cubrid\_close\_prepare
  - function.cubrid-col-get.md: cubrid\_col\_get »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_close\_request
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_close\_request

(PECL CUBRID >= 8.3.0)

cubrid\_close\_request — Закриває обробник запиту

### Опис

```methodsynopsis
cubrid_close_request(resource $req_identifier): bool
```

Функция**cubrid\_close\_request()** закриває обробник запиту, заданий у `req_identifier`, і звільняє виділену йому пам'ять. Є синонімом для [cubrid\_close\_prepare()](function.cubrid-close-prepare.md)

### Список параметрів

`req_identifier`

Ідентифікатор запиту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання.

### Приклади

**Приклад #1 Приклад використання** cubrid\_close\_request()\*\*\*\*

```php
<?php
$con = cubrid_connect ("localhost", 33000, "demodb", "dba", "");
if ($con) {
   echo "connected successfully";
   $req = cubrid_execute ( $con, "select * from members",
                           CUBRID_INCLUDE_OID | CUBRID_ASYNC);
   if ($req) {
      while ( list ($id, $name) = cubrid_fetch ($req) ){
         echo $id;
         echo $name;
      }
      cubrid_close_request($req); // or you can use cubrid_close_prepare($req)
   }
   cubrid_disconnect($con);
}
?>
```

### Дивіться також

-   [cubrid\_close\_prepare()](function.cubrid-close-prepare.md) \- Закриває обробник запиту
