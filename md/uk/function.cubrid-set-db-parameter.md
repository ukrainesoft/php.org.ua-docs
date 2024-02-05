---
navigation:
  - function.cubrid-set-autocommit.md: « cubrid\_set\_autocommit
  - function.cubrid-set-drop.md: cubrid\_set\_drop »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_set\_db\_parameter
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_set\_db\_parameter

(PECL CUBRID >= 8.4.0)

cubrid\_set\_db\_parameter — Встановлює параметри бази даних CUBRID

### Опис

```methodsynopsis
cubrid_set_db_parameter(resource $conn_identifier, int $param_type, int $param_value): bool
```

Функция**cubrid\_set\_db\_parameter()** використовується для встановлення параметрів бази даних CUBRID. Він може встановити такі параметри бази даних CUBRID:

-   **`PARAM_ISOLATION_LEVEL`**
-   **`PARAM_LOCK_TIMEOUT`**

> **Зауваження** :
> 
> Режим автоматичної фіксації може бути встановлений за допомогою [cubrid\_set\_autocommit()](function.cubrid-set-autocommit.md)

### Список параметрів

`conn_identifier`

CUBRID з'єднання. Якщо ідентифікатор з'єднання не вказано, передбачається останнє посилання, що відкривається [cubrid\_connect()](function.cubrid-connect.md)

`param_type`

Тип параметру бази даних.

`param_value`

Значення рівня ізоляції (1-6) або часу очікування блокування (в секундах).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад использования[cubrid\_get\_db\_parameter()](function.cubrid-get-db-parameter.md)**

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

$params = cubrid_get_db_parameter($conn);
var_dump($params);

cubrid_set_autocommit($conn, CUBRID_AUTOCOMMIT_TRUE);
cubrid_set_db_parameter($conn, CUBRID_PARAM_ISOLATION_LEVEL, 2);

$params_new = cubrid_get_db_parameter($conn);
var_dump($params_new);

cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

```
array(4) {
  ["PARAM_ISOLATION_LEVEL"]=>
  int(3)
  ["PARAM_LOCK_TIMEOUT"]=>
  int(-1)
  ["PARAM_MAX_STRING_LENGTH"]=>
  int(1073741823)
  ["PARAM_AUTO_COMMIT"]=>
  int(0)
}
array(4) {
  ["PARAM_ISOLATION_LEVEL"]=>
  int(2)
  ["PARAM_LOCK_TIMEOUT"]=>
  int(-1)
  ["PARAM_MAX_STRING_LENGTH"]=>
  int(1073741823)
  ["PARAM_AUTO_COMMIT"]=>
  int(1)
}
```

### Дивіться також

-   [cubrid\_get\_db\_parameter()](function.cubrid-get-db-parameter.md) \- Повертає параметри бази даних CUBRID
-   [cubrid\_set\_autocommit()](function.cubrid-set-autocommit.md) \- Встановлює режим авто-комміту для з'єднання
