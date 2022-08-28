Отримати інформацію про схему

-   [« PDO\_CUBRID DSN](ref.pdo-cubrid.connection.html)
    
-   [MS SQL Server (PDO\_DBLIB) »](ref.pdo-dblib.html)
    
-   [PHP Manual](index.html)
    
-   [CUBRID (PDO)](ref.pdo-cubrid.html)
    
-   Отримати інформацію про схему
    

# PDO::cubridschema

(PECL PDOCUBRID >= 8.3.0.0001)

PDO::cubridschema — Отримати запитану інформацію про схему

### Опис

```methodsynopsis
public PDO::cubrid_schema(int $schema_type, string $table_name = ?, string $col_name = ?): array
```

Ця функція використовується для отримання інформації про схему бази даних. Якщо необхідна інформація про конкретну таблицю, необхідно буде вказати її ім'я в параметрі `table_name`. Якщо потрібна інформація про конкретний стовпчик таблиці, його ім'я необхідно вказати в параметрі `col_name` (може використовуватись тільки з PDO::CUBRIDSCHCOLPRIVILEGE).

Результат буде повернутий у вигляді двовимірного масиву (стовпець (асоціативний масив)) рядок (асоціативний масив). У наступній таблиці наводяться типи схеми та структура стовпців результуючого масиву, який буде повернутий залежно від типу схеми, що використовується.

**Склад результату кожного типу**

| Схема | Номер столбца | Имя столбца | Значение |
| --- | --- | --- | --- |
| PDO::CUBRIDSCHTABLE |  | NAME |  |
|  |  | TYPE | 0:system table 1:view 2:table |
| PDO::CUBRIDSCHVIEW |  | NAME |  |
|  |  | TYPE | 1:view |
| PDO::CUBRIDSCHQUERYSPEC |  | QUERYSPEC |  |
| PDO::CUBRIDSCHATTRIBUTE / PDO::CUBRIDSCHTABLEATTRIBUTE |  | ATTRNAME |  |
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
| PDO::CUBRIDSCHMETHOD / PDO :: CUBRIDSCHTABLEMETHOD |  | NAME |  |
|  |  | RETDOMAIN |  |
|  |  | ARGDOMAIN |  |
| PDO::CUBRIDSCHMETHODFILE |  | METHODFILE |  |
| PDO::CUBRIDSCHSUPERTABLE / PDO::CUBRIDSCHDIRECTSUPERTABLE / PDO::CUBRIDSCHSUBTABLE |  | CLASSNAME |  |
|  |  | TYPE | 0:system table 1:view 2:table |
| PDO::CUBRIDSCHCONSTRAINT |  | TYPE | 0:unique 1:index 2:reverse unique 3:reverse index |
|  |  | NAME |  |
|  |  | ATTRNAME |  |
|  |  | NUMPAGES |  |
|  |  | NUMKEYS |  |
|  |  | PRIMARYKEY | 1:primary key |
|  |  | KEYORDER | base:1 |
| PDO::CUBRIDSCHTRIGGER |  | NAME |  |
|  |  | STATUS |  |
|  |  | EVENT |  |
|  |  | TARGETCLASS |  |
|  |  | TARGETATTR |  |
|  |  | ACTIONTIME |  |
|  |  | ACTION |  |
|  |  | PRIORITY |  |
|  |  | CONDITIONTIME |  |
|  |  | CONDITION |  |
| PDO::CUBRIDSCHTABLEPRIVILEGE / PDO::CUBRIDSCHCOLPRIVILEGE |  | CLASSNAME/ATTRNAME |  |
|  |  | PRIVILEGE |  |
|  |  | GRANTABLE |  |
| PDO::CUBRIDSCHPRIMARYKEY |  | CLASSNAME |  |
|  |  | ATTRNAME |  |
|  |  | KEYSEQ | base:1 |
|  |  | KEYNAME |  |
| PDO::CUBRIDSCHIMPORTEDKEYS / PDO::CUBRIDSCHEXPORTEDKEYS / PDO::CUBRIDSCHCROSSREFERENCE |  | PKTABLENAME |  |
|  |  | PKCOLUMNNAME |  |
|  |  | FKTABLENAME | base:1 |
|  |  | FKCOLUMNNAME |  |
|  |  | KEYSEQ | base:1 |
|  |  | UPDATEACTION | 0:cascade 1:restrict 2:no action 3:set null |
|  |  | DELETEACTION | 0:cascade 1:restrict 2:no action 3:set null |
|  |  | ФКNAME |  |
|  |  | ПКNAME |  |

### Список параметрів

`schema_type`

Необхідний тип схеми.

`table_name`

Назва таблиці, схему якої ви хочете отримати.

`col_name`

Ім'я шпальти, схему якої ви хочете отримати.

### Значення, що повертаються

У разі успішного виконання буде повернено асоціативний масив зі схемою.

У разі невдачі буде повернено **`false`**

### Приклади

**Приклад #1 Приклад використання **PDO::cubridschema()****

У цьому прикладі демонструється отримання інформації про первинні та вторинні ключі таблиці "game".

```php
<?php
$pk_list = $dbh->cubrid_schema(PDO::CUBRID_SCH_PRIMARY_KEY, "game");
print_r($pk_list);

$fk_list = $dbh->cubrid_schema(PDO::CUBRID_SCH_IMPORTED_KEYS, "game");
print_r($fk_list);
?>
```

Результат виконання цього прикладу:

```
Result:
Array
(
    [0] => Array
        (
            [CLASS_NAME] => game
            [ATTR_NAME] => athlete_code
            [KEY_SEQ] => 3
            [KEY_NAME] => pk_game_host_year_event_code_athlete_code
        )

    [1] => Array
        (
            [CLASS_NAME] => game
            [ATTR_NAME] => event_code
            [KEY_SEQ] => 2
            [KEY_NAME] => pk_game_host_year_event_code_athlete_code
        )

    [2] => Array
        (
            [CLASS_NAME] => game
            [ATTR_NAME] => host_year
            [KEY_SEQ] => 1
            [KEY_NAME] => pk_game_host_year_event_code_athlete_code
        )

)
Array
(
    [0] => Array
        (
            [PKTABLE_NAME] => athlete
            [PKCOLUMN_NAME] => code
            [FKTABLE_NAME] => game
            [FKCOLUMN_NAME] => athlete_code
            [KEY_SEQ] => 1
            [UPDATE_RULE] => 1
            [DELETE_RULE] => 1
            [FK_NAME] => fk_game_athlete_code
            [PK_NAME] => pk_athlete_code
        )

    [1] => Array
        (
            [PKTABLE_NAME] => event
            [PKCOLUMN_NAME] => code
            [FKTABLE_NAME] => game
            [FKCOLUMN_NAME] => event_code
            [KEY_SEQ] => 1
            [UPDATE_RULE] => 1
            [DELETE_RULE] => 1
            [FK_NAME] => fk_game_event_code
            [PK_NAME] => pk_event_code
        )

)
```