---
navigation:
  - function.cubrid-connect.md: « cubrid\_connect
  - function.cubrid-disconnect.md: cubrid\_disconnect »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_current\_oid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_current\_oid

(PECL CUBRID >= 8.3.0)

cubrid\_current\_oid — Повертає OID поточної позиції курсору

### Опис

```methodsynopsis
cubrid_current_oid(resource $req_identifier): string
```

Функция**cubrid\_current\_oid()** використовується для одержання oid поточного положення курсору в результуючому наборі. Для використання функції **cubrid\_current\_oid()**, запущений запит повинен бути оновлюваним, і при запуску запиту було встановлено опцію **`CUBRID_INCLUDE_OID`**

### Список параметрів

`req_identifier`

Ідентифікатор запиту.

### Значення, що повертаються

Oid поточного положення курсору, у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**cubrid\_current\_oid()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

$req = cubrid_execute($conn, "SELECT * FROM code", CUBRID_INCLUDE_OID);
$oid = cubrid_current_oid($req);
$res = cubrid_get($conn, $oid);

print_r($res);

cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [s_name] => X
    [f_name] => Mixed
)
```

### Дивіться також

-   [cubrid\_execute()](function.cubrid-execute.md) \- Виконує підготовлений SQL-оператор
