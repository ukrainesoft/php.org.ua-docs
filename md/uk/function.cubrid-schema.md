---
navigation:
  - function.cubrid-rollback.md: « cubrid\_rollback
  - function.cubrid-seq-drop.md: cubrid\_seq\_drop »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_schema
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_schema

(PECL CUBRID >= 8.3.0)

cubrid\_schema — Отримує запитану інформацію про схему

### Опис

```methodsynopsis
cubrid_schema(    resource $conn_identifier,    int $schema_type,    string $class_name = ?,    string $attr_name = ?): array
```

Функция**cubrid\_schema()** використовується для отримання запитаної інформації про схему бази даних. Ви повинні вказати `class_name`, якщо ви хочете отримати інформацію про певний клас, `attr_name`, якщо ви хочете отримати інформацію про певний атрибут (може використовуватись тільки з **`CUBRID_SCH_ATTR_PRIVILEGE`**

Результат функции**cubrid\_schema()** повертається у вигляді двовимірного масиву (стовпець (асоціативний масив)) \* рядок (числовий масив)). У наступних таблицях показані типи схем та структура стовпців результуючого масиву, які мають бути повернуті на основі типу схеми.

**Склад результату кожного типу**

| Схема | Номер столбца | Имя столбца | Значение |
| --- | --- | --- | --- |
| CUBRID\_SCH\_CLASS |  | NAME |  |
|  |  | TYPE | 0:system class 1:vclass 2:class |
| CUBRID\_SCH\_VCLASS |  | NAME |  |
|  |  | TYPE | 1:vclass |
| CUBRID\_SCH\_QUERY\_SPEC |  | QUERY\_SPEC |  |
| CUBRID\_SCH\_ATTRIBUTE / CUBRID\_SCH\_CLASS\_ATTRIBUTE |  | ATTR\_NAME |  |
|  |  | DOMAIN |  |
|  | 3 | SCALE |  |
|  | 4 | PRECISION |  |
|  | 5 | INDEXED | 1:indexed |
|  | 6 | NOT NULL | 1:not null |
|  | 7 | SHARED | 1:shared |
|  | 8 | UNIQUE | 1:unique |
|  | 9 | DEFAULT |  |
|  | 10 | ATTR\_ORDER | base:1 |
|  | 11 | CLASS\_NAME |  |
|  | 12 | SOURCE\_CLASS |  |
|  | 13 | IS\_KEY | 1:key |
| CUBRID\_SCH\_METHOD / CUBRID\_SCH\_CLASS\_METHOD |  | NAME |  |
|  |  | RET\_DOMAIN |  |
|  | 3 | ARG\_DOMAIN |  |
| CUBRID\_SCH\_METHOD\_FILE |  | METHOD\_FILE |  |
| CUBRID\_SCH\_SUPERCLASS / CUBRID\_SCH\_DIRECT\_SUPER\_CLASS / CUBRID\_SCH\_SUBCLASS |  | CLASS\_NAME |  |
|  |  | TYPE | 0:system class 1:vclass 2:class |
| CUBRID\_SCH\_CONSTRAINT |  | TYPE | 0:unique 1:index 2:reverse unique 3:reverse index |
|  |  | NAME |  |
|  | 3 | ATTR\_NAME |  |
|  | 4 | NUM\_PAGES |  |
|  | 5 | NUM\_KEYS |  |
|  | 6 | PRIMARY\_KEY | 1:primary key |
|  | 7 | KEY\_ORDER | base:1 |
| CUBRID\_SCH\_TRIGGER |  | NAME |  |
|  |  | STATUS |  |
|  | 3 | EVENT |  |
|  | 4 | TARGET\_CLASS |  |
|  | 5 | TARGET\_ATTR |  |
|  | 6 | ACTION\_TIME |  |
|  | 7 | ACTION |  |
|  | 8 | PRIORITY |  |
|  | 9 | CONDITION\_TIME |  |
|  | 10 | CONDITION |  |
| CUBRID\_SCH\_CLASS\_PRIVILEGE / CUBRID\_SCH\_ATTR\_PRIVILEGE |  | CLASS\_NAME / ATTR\_NAME |  |
|  |  | PRIVILEGE |  |
|  | 3 | GRANTABLE |  |
| CUBRID\_SCH\_PRIMARY\_KEY |  | CLASS\_NAME |  |
|  |  | ATTR\_NAME |  |
|  | 3 | KEY\_SEQ | base:1 |
|  | 4 | KEY\_NAME |  |
| CUBRID\_SCH\_IMPORTED\_KEYS / CUBRID\_SCH\_EXPORTED\_KEYS / CUBRID\_SCH\_CROSS\_REFERENCE |  | PKTABLE\_NAME |  |
|  |  | PKCOLUMN\_NAME |  |
|  | 3 | FKTABLE\_NAME | base:1 |
|  | 4 | FKCOLUMN\_NAME |  |
|  | 5 | KEY\_SEQ | base:1 |
|  | 6 | UPDATE\_ACTION | 0:cascade 1:restrict 2:no action 3:set null |
|  | 7 | DELETE\_ACTION | 0:cascade 1:restrict 2:no action 3:set null |
|  | 8 | FK\_NAME |  |
|  | 9 | PK\_NAME |  |

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`schema_type`

Дані схеми, які ви хочете дізнатися.

`class_name`

Клас, для якого ви хочете дізнатися про схему.

`attr_name`

Атрибут, для якого ви хочете дізнатися про схему.

### Значення, що повертаються

Масив, що містить інформацію про схему, у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.1 | Змінено значення, що повертається: якщо процес завершився з помилкою, повертається false, а не -1. |

### Приклади

**Приклад #1 Приклад використання** cubrid\_schema()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

printf("\n--- Первичный ключ ---\n");
$pk = cubrid_schema($conn, CUBRID_SCH_PRIMARY_KEY, "game");
var_dump($pk);

printf("\n--- Внешние ключи ---\n");
$fk = cubrid_schema($conn, CUBRID_SCH_IMPORTED_KEYS, "game");
var_dump($fk);

printf("\n--- Атрибут столбца ---\n");
$attr = cubrid_schema($conn, CUBRID_SCH_ATTRIBUTE, "stadium", "area");
var_dump($attr);

cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

```
--- Первичный ключ ---
array(3) {
  [0]=>
  array(4) {
    ["CLASS_NAME"]=>
    string(4) "game"
    ["ATTR_NAME"]=>
    string(12) "athlete_code"
    ["KEY_SEQ"]=>
    string(1) "3"
    ["KEY_NAME"]=>
    string(41) "pk_game_host_year_event_code_athlete_code"
  }
  [1]=>
  array(4) {
    ["CLASS_NAME"]=>
    string(4) "game"
    ["ATTR_NAME"]=>
    string(10) "event_code"
    ["KEY_SEQ"]=>
    string(1) "2"
    ["KEY_NAME"]=>
    string(41) "pk_game_host_year_event_code_athlete_code"
  }
  [2]=>
  array(4) {
    ["CLASS_NAME"]=>
    string(4) "game"
    ["ATTR_NAME"]=>
    string(9) "host_year"
    ["KEY_SEQ"]=>
    string(1) "1"
    ["KEY_NAME"]=>
    string(41) "pk_game_host_year_event_code_athlete_code"
  }
}

--- Внешние ключи ---
array(2) {
  [0]=>
  array(9) {
    ["PKTABLE_NAME"]=>
    string(7) "athlete"
    ["PKCOLUMN_NAME"]=>
    string(4) "code"
    ["FKTABLE_NAME"]=>
    string(4) "game"
    ["FKCOLUMN_NAME"]=>
    string(12) "athlete_code"
    ["KEY_SEQ"]=>
    string(1) "1"
    ["UPDATE_RULE"]=>
    string(1) "1"
    ["DELETE_RULE"]=>
    string(1) "1"
    ["FK_NAME"]=>
    string(20) "fk_game_athlete_code"
    ["PK_NAME"]=>
    string(15) "pk_athlete_code"
  }
  [1]=>
  array(9) {
    ["PKTABLE_NAME"]=>
    string(5) "event"
    ["PKCOLUMN_NAME"]=>
    string(4) "code"
    ["FKTABLE_NAME"]=>
    string(4) "game"
    ["FKCOLUMN_NAME"]=>
    string(10) "event_code"
    ["KEY_SEQ"]=>
    string(1) "1"
    ["UPDATE_RULE"]=>
    string(1) "1"
    ["DELETE_RULE"]=>
    string(1) "1"
    ["FK_NAME"]=>
    string(18) "fk_game_event_code"
    ["PK_NAME"]=>
    string(13) "pk_event_code"
  }
}

--- Атрибут столбца ---
array(1) {
  [0]=>
  array(13) {
    ["ATTR_NAME"]=>
    string(4) "area"
    ["DOMAIN"]=>
    string(1) "7"
    ["SCALE"]=>
    string(1) "2"
    ["PRECISION"]=>
    string(2) "10"
    ["INDEXED"]=>
    string(1) "0"
    ["NON_NULL"]=>
    string(1) "0"
    ["SHARED"]=>
    string(1) "0"
    ["UNIQUE"]=>
    string(1) "0"
    ["DEFAULT"]=>
    NULL
    ["ATTR_ORDER"]=>
    string(1) "4"
    ["CLASS_NAME"]=>
    string(7) "stadium"
    ["SOURCE_CLASS"]=>
    string(7) "stadium"
    ["IS_KEY"]=>
    string(1) "0"
  }
}
```
