---
navigation:
  - function.cubrid-bind.md: « cubrid\_bind
  - function.cubrid-close-request.md: cubrid\_close\_request »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_close\_prepare
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_close\_prepare

(PECL CUBRID >= 8.3.0)

cubrid\_close\_prepare — Закриває обробник запиту

### Опис

```methodsynopsis
cubrid_close_prepare(resource $req_identifier): bool
```

Функция**cubrid\_close\_prepare()** закриває обробник запиту, заданий у `req_identifier`, і звільняє виділену йому пам'ять. Є синонімом для [cubrid\_close\_request()](function.cubrid-close-request.md)

### Список параметрів

`req_identifier`

Ідентифікатор запиту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання.

### Приклади

**Пример #1 Пример использования**cubrid\_close\_prepare()\*\*\*\*

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

-   [cubrid\_close\_request()](function.cubrid-close-request.md) \- Закриває обробник запиту
