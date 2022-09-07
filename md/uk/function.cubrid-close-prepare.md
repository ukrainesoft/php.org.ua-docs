---
navigation:
  - function.cubrid-bind.md: « cubridbind
  - function.cubrid-close-request.md: cubridcloserequest »
  - index.md: PHP Manual
  - ref.cubrid.md: Функции CUBRID
title: cubridcloseprepare
---
# cubridcloseprepare

(PECL CUBRID >= 8.3.0)

cubridcloseprepare — Закриває обробник запиту

### Опис

```methodsynopsis
cubrid_close_prepare(resource $req_identifier): bool
```

Функція **cubridcloseprepare()** закриває обробник запиту, заданий у `req_identifier`, і звільняє виділену йому пам'ять. Є синонімом для [cubridcloserequest()](function.cubrid-close-request.md)

### Список параметрів

`req_identifier`

Ідентифікатор запиту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання.

### Приклади

**Приклад #1 Приклад використання **cubridcloseprepare()****

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
      cubrid_close_prepare($req); // or you can use cubrid_close_request($req)
   }
   cubrid_disconnect($con);
}
?>
```

### Дивіться також

-   [cubridcloserequest()](function.cubrid-close-request.md) - Закриває обробник запиту
