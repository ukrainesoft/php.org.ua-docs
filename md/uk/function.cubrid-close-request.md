---
navigation:
  - function.cubrid-close-prepare.html: « cubridcloseprepare
  - function.cubrid-col-get.html: cubridcolget »
  - index.md: PHP Manual
  - ref.cubrid.md: Функции CUBRID
title: cubridcloserequest
---
# cubridcloserequest

(PECL CUBRID >= 8.3.0)

cubridcloserequest — Закриває обробник запиту

### Опис

```methodsynopsis
cubrid_close_request(resource $req_identifier): bool
```

Функція **cubridcloserequest()** закриває обробник запиту, заданий у `req_identifier`, і звільняє виділену йому пам'ять. Є синонімом для [cubridcloseprepare()](function.cubrid-close-prepare.md)

### Список параметрів

`req_identifier`

Ідентифікатор запиту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання.

### Приклади

**Приклад #1 Приклад використання **cubridcloserequest()****

```php
<?php
$con = cubrid_connect ("localhost", 33000, "demodb", "dba", "");
if ($con) {
   echo "connected successfully";
   $req = cubrid_execute ( $con, "select * from members",
                           CUBRID_INCLUDE_OID | CUBRID_ASYNC);
   if ($req) {
      while ( list ($id, $name) = cubrid_fetch ($req) ){
         echo $id;
         echo $name;
      }
      cubrid_close_request($req); // or you can use cubrid_close_prepare($req)
   }
   cubrid_disconnect($con);
}
?>
```

### Дивіться також

-   [cubridcloseprepare()](function.cubrid-close-prepare.md) - Закриває обробник запиту
