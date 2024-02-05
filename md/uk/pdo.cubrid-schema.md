---
navigation:
  - ref.pdo-cubrid.connection.md: « PDO\_CUBRID DSN
  - ref.pdo-dblib.md: MS SQL Server (PDO\_DBLIB) »
  - index.md: PHP Manual
  - ref.pdo-cubrid.md: CUBRID (PDO)
title: 'PDO::cubrid\_schema'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDO::cubrid\_schema

(PECL PDO\_CUBRID >= 8.3.0.0001)

PDO::cubrid\_schema — Отримати запитану інформацію про схему

### Опис

```methodsynopsis
public PDO::cubrid_schema(int $schema_type, string $table_name = ?, string $col_name = ?): array
```

Ця функція використовується для отримання інформації про схему бази даних. Якщо необхідна інформація про конкретну таблицю, необхідно буде вказати її ім'я в параметрі `table_name`. Якщо потрібна інформація про конкретний стовпчик таблиці, його ім'я необхідно вказати в параметрі `col_name` (може використовуватись тільки з PDO::CUBRID\_SCH\_COL\_PRIVILEGE).

Результат буде повернутий у вигляді двовимірного масиву (стовпець (асоціативний масив)) \* рядок (асоціативний масив). У наступній таблиці наводяться типи схеми та структура стовпців результуючого масиву, який буде повернутий залежно від типу схеми, що використовується.

**Склад результату кожного типу**

| Схема | Номер столбца | Имя столбца | Значение |
| --- | --- | --- | --- |
| PDO::CUBRID\_SCH\_TABLE |  | NAME |  |
|  |  | TYPE | 0:system table 1:view 2:table |
| PDO::CUBRID\_SCH\_VIEW |  | NAME |  |
|  |  | TYPE | 1:view |
| PDO::CUBRID\_SCH\_QUERY\_SPEC |  | QUERY\_SPEC |  |
| PDO::CUBRID\_SCH\_ATTRIBUTE / PDO::CUBRID\_SCH\_TABLE\_ATTRIBUTE |  | ATTR\_NAME |  |
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
| PDO::CUBRID\_SCH\_METHOD / PDO::CUBRID\_SCH\_TABLE\_METHOD |  | NAME |  |
|  |  | RET\_DOMAIN |  |
|  | 3 | ARG\_DOMAIN |  |
| PDO::CUBRID\_SCH\_METHOD\_FILE |  | METHOD\_FILE |  |
| PDO::CUBRID\_SCH\_SUPER\_TABLE / PDO::CUBRID\_SCH\_DIRECT\_SUPER\_TABLE / PDO::CUBRID\_SCH\_SUB\_TABLE |  | CLASS\_NAME |  |
|  |  | TYPE | 0:system table 1:view 2:table |
| PDO::CUBRID\_SCH\_CONSTRAINT |  | TYPE | 0:unique 1:index 2:reverse unique 3:reverse index |
|  |  | NAME |  |
|  | 3 | ATTR\_NAME |  |
|  | 4 | NUM\_PAGES |  |
|  | 5 | NUM\_KEYS |  |
|  | 6 | PRIMARY\_KEY | 1:primary key |
|  | 7 | KEY\_ORDER | base:1 |
| PDO::CUBRID\_SCH\_TRIGGER |  | NAME |  |
|  |  | STATUS |  |
|  | 3 | EVENT |  |
|  | 4 | TARGET\_CLASS |  |
|  | 5 | TARGET\_ATTR |  |
|  | 6 | ACTION\_TIME |  |
|  | 7 | ACTION |  |
|  | 8 | PRIORITY |  |
|  | 9 | CONDITION\_TIME |  |
|  | 10 | CONDITION |  |
| PDO::CUBRID\_SCH\_TABLE\_PRIVILEGE / PDO::CUBRID\_SCH\_COL\_PRIVILEGE |  | CLASS\_NAME / ATTR\_NAME |  |
|  |  | PRIVILEGE |  |
|  | 3 | GRANTABLE |  |
| PDO::CUBRID\_SCH\_PRIMARY\_KEY |  | CLASS\_NAME |  |
|  |  | ATTR\_NAME |  |
|  | 3 | KEY\_SEQ | base:1 |
|  | 4 | KEY\_NAME |  |
| PDO::CUBRID\_SCH\_IMPORTED\_KEYS / PDO::CUBRID\_SCH\_EXPORTED\_KEYS / PDO::CUBRID\_SCH\_CROSS\_REFERENCE |  | PKTABLE\_NAME |  |
|  |  | PKCOLUMN\_NAME |  |
|  | 3 | FKTABLE\_NAME | base:1 |
|  | 4 | FKCOLUMN\_NAME |  |
|  | 5 | KEY\_SEQ | base:1 |
|  | 6 | UPDATE\_ACTION | 0:cascade 1:restrict 2:no action 3:set null |
|  | 7 | DELETE\_ACTION | 0:cascade 1:restrict 2:no action 3:set null |
|  | 8 | FK\_NAME |  |
|  | 9 | PK\_NAME |  |

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

**Приклад #1 Приклад використання** PDO::cubrid\_schema()\*\*\*\*

У цьому прикладі демонструється отримання інформації про первинні та вторинні ключі таблиці "game".

```php
<?php
$pk_list = $dbh->cubrid_schema(PDO::CUBRID_SCH_PRIMARY_KEY, "game");
print_r($pk_list);

$fk_list = $dbh->cubrid_schema(PDO::CUBRID_SCH_IMPORTED_KEYS, "game");
print_r($fk_list);
?>
```

Результат виконання наведеного прикладу:

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
