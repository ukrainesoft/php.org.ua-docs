---
navigation:
  - function.cubrid-lob-size.md: « cubrid\_lob\_size
  - function.cubrid-lob2-close.md: cubrid\_lob2\_close »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_lob2\_bind
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_lob2\_bind

(PECL CUBRID >= 8.4.1)

cubrid\_lob2\_bind — Зв'язує об'єкт LOB або рядок у вигляді об'єкта LOB з підготовленим оператором як параметри

### Опис

```methodsynopsis
cubrid_lob2_bind(    resource $req_identifier,    int $bind_index,    mixed $bind_value,    string $bind_value_type = ?): bool
```

Функция**cubrid\_lob2\_bind()** використовується для прив'язки даних BLOB/CLOB до відповідної псевдозмінної оператора SQL, який був переданий в [cubrid\_prepare()](function.cubrid-prepare.md). Якщо параметр `bind_value_type` не вказано, за промовчанням буде використовуватися рядок "BLOB". Але якщо раніше використовувалась функція [cubrid\_lob2\_new()](function.cubrid-lob2-new.md) `bind_value_type` буде відповідати параметру `type`в[cubrid\_lob2\_new()](function.cubrid-lob2-new.md)по умолчанию.

### Список параметрів

`req_identifier`

Ідентифікатор запиту, отриманий у результаті роботи [cubrid\_prepare()](function.cubrid-prepare.md)

`bind_index`

Розташування параметрів прив'язування. Починається з першого.

`bind_value`

Фактичне значення для прив'язування.

`bind_value_type`

Значення має дорівнювати "BLOB" або "CLOB", регістр не враховується. Якщо значення не вказано, за промовчанням використовується "BLOB".

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_lob2\_bind()\*\*\*\*

```php
<?php
// Таблица: test_lob (id INT, contents CLOB)

$conn = cubrid_connect("localhost", 33000, "demodb", "dba", "");

cubrid_execute($conn,"DROP TABLE if exists test_lob");
cubrid_execute($conn,"CREATE TABLE test_lob (id INT, contents CLOB)");

$req = cubrid_prepare($conn, "INSERT INTO test_lob VALUES (?, ?)");

cubrid_bind($req,1, 3);

$lob = cubrid_lob2_new($conn, 'CLOB');
cubrid_lob2_bind($req, 2, $lob);

cubrid_execute($req);

cubrid_bind($req, 1, 4);

cubrid_lob2_bind($req, 2, 'CUBRID LOB2 TEST', 'CLOB');

cubrid_execute($req);

cubrid_disconnect($conn);
?>
```

### Дивіться також

-   [cubrid\_lob2\_new()](function.cubrid-lob2-new.md) \- Створює об'єкт LOB
-   [cubrid\_lob2\_close()](function.cubrid-lob2-close.md) \- Закриває об'єкт LOB
