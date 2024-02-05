---
navigation:
  - function.cubrid-get-charset.md: « cubrid\_get\_charset
  - function.cubrid-get-client-info.md: cubrid\_get\_client\_info »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_get\_class\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_get\_class\_name

(PECL CUBRID >= 8.3.0)

cubrid\_get\_class\_name — Отримує ім'я класу за допомогою OID

### Опис

```methodsynopsis
cubrid_get_class_name(resource $conn_identifier, string $oid): string
```

Функция\*\*cubrid\_get\_class\_name()\*\*используется для получения имени класса из параметра`oid`. Не працює при виборі даних із системних таблиць, наприклад db\_class.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`oid`

OID екземпляра, існування якого необхідно перевірити.

### Значення, що повертаються

Имя класса при успешном завершении процесса или\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_get\_class\_name()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

$req = cubrid_execute($conn, "SELECT * FROM code", CUBRID_INCLUDE_OID);
$oid = cubrid_current_oid($req);
$class_name = cubrid_get_class_name($conn, $oid);

print_r($class_name);

cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

```
code
```

### Дивіться також

-   [cubrid\_is\_instance()](function.cubrid-is-instance.md) \- Перевіряє, чи існує екземпляр, на який вказує OID
-   [cubrid\_drop()](function.cubrid-drop.md) \- Видалення екземпляра за OID
