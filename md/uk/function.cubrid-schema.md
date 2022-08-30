Отримує запитану інформацію про схему

-   [« cubridrollback](function.cubrid-rollback.html)
    
-   [cubridseqdrop »](function.cubrid-seq-drop.html)
    
-   [PHP Manual](index.md)
    
-   [Функции CUBRID](ref.cubrid.md)
    
-   Отримує запитану інформацію про схему
    

# cubridschema

(PECL CUBRID >= 8.3.0)

cubridschema — Отримує запитану інформацію про схему

### Опис

```methodsynopsis
cubrid_schema(    resource $conn_identifier,    int $schema_type,    string $class_name = ?,    string $attr_name = ?): array
```

Функція **cubridschema()** використовується для отримання запитаної інформації про схему бази даних. Ви повинні вказати `class_name`, якщо ви хочете отримати інформацію про певний клас, `attr_name`, якщо ви хочете отримати інформацію про певний атрибут (може використовуватися тільки з **`CUBRID_SCH_ATTR_PRIVILEGE`**

Результат функції **cubridschema()** повертається у вигляді двовимірного масиву (стовпець (асоціативний масив)) рядок (числовий масив)). У наступних таблицях показані типи схем та структура стовпців результуючого масиву, які мають бути повернуті на основі типу схеми.

**Склад результату кожного типу**

| Схема | Номер столбца | Имя столбца | Значение |
| --- | --- | --- | --- |
| CUBRIDSCHCLASS |  | NAME |  |
|  |  | TYPE | 0:system class 1:vclass 2:class |
| CUBRIDSCHVCLASS |  | NAME |  |
|  |  | TYPE | 1:vclass |
| CUBRIDSCHQUERYSPEC |  | QUERYSPEC |  |
| CUBRIDSCHATTRIBUTE/CUBRIDSCHCLASSATTRIBUTE |  | ATTRNAME |  |
|  |  | DOMAIN |  |
|  |  | SCALE |  |
|  |  | PRECISION |  |
|  |  | INDEXED | 1:indexed |
|  |  | NOT NULL | 1:not null |
|  |  | SHARED | 1:shared |
|  |  | UNIQUE | 1: unique |
|  |  | DEFAULT |  |
|  |  | ATTRORDER | base:1 |
|  |  | CLASSNAME |  |
|  |  | SOURCECLASS |  |
|  |  | ІСKEY | 1:key |
| CUBRIDSCHMETHOD/CUBRIDSCHCLASSMETHOD |  | NAME |  |
|  |  | RETDOMAIN |  |
|  |  | ARGDOMAIN |  |
| CUBRIDSCHMETHODFILE |  | METHODFILE |  |
| CUBRIDSCHSUPERCLASS/CUBRIDSCHDIRECTSUPERCLASS/CUBRIDSCHSUBCLASS |  | CLASSNAME |  |
|  |  | TYPE | 0:system class 1:vclass 2:class |
| CUBRIDSCHCONSTRAINT |  | TYPE | 0:unique 1:index 2:reverse unique 3:reverse index |
|  |  | NAME |  |
|  |  | ATTRNAME |  |
|  |  | NUMPAGES |  |
|  |  | NUMKEYS |  |
|  |  | PRIMARYKEY | 1:primary key |
|  |  | KEYORDER | base:1 |
| CUBRIDSCHTRIGGER |  | NAME |  |
|  |  | STATUS |  |
|  |  | EVENT |  |
|  |  | TARGETCLASS |  |
|  |  | TARGETATTR |  |
|  |  | ACTIONTIME |  |
|  |  | ACTION |  |
|  |  | PRIORITY |  |
|  |  | CONDITIONTIME |  |
|  |  | CONDITION |  |
| CUBRIDSCHCLASSPRIVILEGE/CUBRIDSCHATTRPRIVILEGE |  | CLASSNAME/ATTRNAME |  |
|  |  | PRIVILEGE |  |
|  |  | GRANTABLE |  |
| CUBRIDSCHPRIMARYKEY |  | CLASSNAME |  |
|  |  | ATTRNAME |  |
|  |  | KEYSEQ | base:1 |
|  |  | KEYNAME |  |
| CUBRIDSCHIMPORTEDKEYS/CUBRIDSCHEXPORTEDKEYS/CUBRIDSCHCROSSREFERENCE |  | PKTABLENAME |  |
|  |  | PKCOLUMNNAME |  |
|  |  | FKTABLENAME | base:1 |
|  |  | FKCOLUMNNAME |  |
|  |  | KEYSEQ | base:1 |
|  |  | UPDATEACTION | 0:cascade 1:restrict 2:no action 3:set null |
|  |  | DELETEACTION | 0:cascade 1:restrict 2:no action 3:set null |
|  |  | ФКNAME |  |
|  |  | ПКNAME |  |

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

Масив, що містить інформацію про схему, у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Змінено значення, що повертається: якщо процес завершився з помилкою, повертається false, а не -1. |

### Приклади

**Приклад #1 Приклад використання **cubridschema()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

printf("\n--- Первичный ключ ---\n");
$pk = cubrid_schema($conn, CUBRID_SCH_PRIMARY_KEY, "game");
var_dump($pk);

printf("\n--- Внешние ключи ---\n");
$fk = cubrid_schema($conn, CUBRID_SCH_IMPORTED_KEYS, "game");
var_dump($fk);

printf("\n--- Атрибут столбца ---\n");
$attr = cubrid_schema($conn, CUBRID_SCH_ATTRIBUTE, "stadium", "area");
var_dump($attr);

cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

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