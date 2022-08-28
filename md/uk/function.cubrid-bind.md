Зв'язує змінні із підготовленим запитом

-   [« Функции CUBRID](ref.cubrid.html)
    
-   [cubrid\_close\_prepare »](function.cubrid-close-prepare.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CUBRID](ref.cubrid.html)
    
-   Зв'язує змінні із підготовленим запитом
    

# cubridbind

(PECL CUBRID >= 8.3.0)

cubridbind — Зв'язує змінні із підготовленим запитом

### Опис

```methodsynopsis
cubrid_bind(    resource $req_identifier,    int $bind_index,    mixed $bind_value,    string $bind_value_type = ?): bool
```

Функція **cubridbind()** використовується для прив'язки значень до зазначених міток, або знаків питання, в SQL-запиті, заданому [cubrid\_prepare()](function.cubrid-prepare.html). Якщо не встановлено параметр `bind_value_type`, то буде використовуватися рядковий тип.

> **Зауваження**
> 
> Якщо дані, що прив'язуються, мають тип BLOB/CLOB, CUBRID спробує використовувати їх як потоки PHP. Якщо фактичне значення, що прив'язується не є потоком, то CUBRID конвертує його в рядок і буде вважати повним шляхом до файлу, де ці дані лежать.
> 
> Якщо тип даних, які будуть пов'язані явно, є ENUM, то параметр `bind_value` має бути елементом ENUM заданим у вигляді рядка.
> 
> В оточенні сегмента CUBRID, `bind_value_type` має бути включений у функцію **cubridbind()**

У наступній таблиці наведено типи замінних значень.

**Прив'язка типів у CUBRID**

| Уровень поддержки | Тип привязки | Соответствующий SQL-тип |
| --- | --- | --- |
| Підтримується | STRING | CHAR, VARCHAR |
|  | NCHAR | NCHAR, NVARCHAR |
|  | BIT | BIT, VARBIT |
|  | NUMERIC or NUMBER | SHORT, INT, NUMERIC |
|  | FLOAT | FLOAT |
|  | DOUBLE | DOUBLE |
|  | TIME | TIME |
|  | DATE | DATE |
|  | TIMESTAMP | TIMESTAMP |
|  | OBJECT | OBJECT |
|  | ENUM | ENUM |
|  | BLOB | BLOB |
|  | CLOB | CLOB |
|  | NULL | NULL |
| Не підтримується | SET | SET |
|  | MULTISET | MULTISET |
|  | SEQUENCE | SEQUENCE |

### Список параметрів

`req_identifier`

Ідентифікатор запиту, отриманий з [cubrid\_prepare()](function.cubrid-prepare.html)

`bind_index`

Розташування параметрів, що зв'язуються. Починаються з першого.

`bind_value`

Фактичне значення для прив'язування.

`bind_value_type`

Тип зв'язуваного значення. (За замовчуванням не встановлено. Таким чином, за замовчуванням використовується тип STRING. Однак, ви повинні явно вказати тип для значень NCHAR, BIT, або BLOB/CLOB).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Додано підтримку типів даних BLOB/CLOB. |

### Приклади

**Приклад #1 Приклад використання **cubridbind()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

$result = cubrid_execute($conn, "SELECT code FROM event WHERE sports='Basketball' and gender='M'");
$row = cubrid_fetch_array($result, CUBRID_ASSOC);
$event_code = $row["code"];

cubrid_close_request($result);

$game_req = cubrid_prepare($conn, "SELECT athlete_code FROM game WHERE host_year=1992 and event_code=? and nation_code='USA'");
cubrid_bind($game_req, 1, $event_code, "number");
cubrid_execute($game_req);

printf("--- Dream Team (1992 United States men's Olympic basketball team) ---\n");
while ($athlete_code = cubrid_fetch_array($game_req, CUBRID_NUM)) {
    $athlete_req = cubrid_prepare($conn, "SELECT name FROM athlete WHERE code=? AND nation_code='USA' AND event='Basketball' AND gender='M'");
    cubrid_bind($athlete_req, 1, $athlete_code[0], "number");
    cubrid_execute($athlete_req);
    $row = cubrid_fetch_assoc($athlete_req);
    printf("%s\n", $row["name"]);
}

cubrid_close_request($game_req);
cubrid_close_request($athlete_req);

cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

```
--- Dream Team (1992 United States men's Olympic basketball team) ---
Stockton John
Robinson David
Pippen Scottie
Mullin C.
Malone Karl
Laettner C.
Jordan Michael
Johnson Earvin
Ewing Patrick
Drexler Clyde
Bird Larry
Barkley Charles
```

**Приклад #2 Приклад використання **cubridbind()** з BLOB/CLOB**

```php
<?php
$con = cubrid_connect("localhost", 33000, "demodb", "dba", "");
if ($con) {
    cubrid_execute($con,"DROP TABLE if exists php_cubrid_lob_test");
    cubrid_execute($con,"CREATE TABLE php_cubrid_lob_test (doc_content CLOB)");
    $sql = "INSERT INTO php_cubrid_lob_test(doc_content) VALUES(?)";
    $req = cubrid_prepare($con, $sql);

    $fp = fopen("book.txt", "rb");

    cubrid_bind($req, 1, $fp, "clob");
    cubrid_execute($req);
}
?>
```

**Приклад #3 Приклад використання **cubridbind()** з BLOB/CLOB**

```php
<?php
$con = cubrid_connect("localhost", 33000, "demodb", "dba", "");
if ($con) {
    cubrid_execute($con,"DROP TABLE if exists php_cubrid_lob_test");
    cubrid_execute($con,"CREATE TABLE php_cubrid_lob_test (image BLOB)");
    $sql = "INSERT INTO php_cubrid_lob_test(image) VALUES(?)";
    $req = cubrid_prepare($con, $sql);

    cubrid_bind($req, 1, "cubrid_logo.png", "blob");
    cubrid_execute($req);
}
?>
```

### Дивіться також

-   [cubrid\_execute()](function.cubrid-execute.html) - Виконує підготовлений SQL-оператор
-   [cubrid\_prepare()](function.cubrid-prepare.html) - Підготовляє SQL-вираз до виконання