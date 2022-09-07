---
navigation:
  - function.db2-escape-string.md: « db2escapestring
  - function.db2-execute.md: db2execute »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2exec
---
# db2exec

(PECL ibmdb2> = 1.0.0)

db2exec — Виконує SQL-запит безпосередньо

### Опис

```methodsynopsis
db2_exec(resource $connection, string $statement, array $options = ?): resource
```

Виконує SQL-запит безпосередньо.

Якщо ви плануєте інтерполювати змінні PHP у SQL-запит, майте на увазі, що це одна з найпоширеніших уразливостей безпеки. Розгляньте можливість виклику [db2prepare()](function.db2-prepare.md) для підготовки SQL запиту з маркерами параметрів для вхідних значень. Потім ви можете викликати [db2execute()](function.db2-execute.md), щоб передати вхідні значення та уникнути атак SQL-ін'єкцій.

Якщо ви плануєте багаторазово виконувати один і той же SQL-запит з різними параметрами, розгляньте можливість виклику [db2prepare()](function.db2-prepare.md) і [db2execute()](function.db2-execute.md), щоб сервер бази даних міг повторно використати свій план доступу та підвищити ефективність вашої бази даних.

### Список параметрів

`connection`

Допустима змінна ресурсу з'єднання з базою даних, що повертається функцією [db2connect()](function.db2-connect.md) або [db2pconnect()](function.db2-pconnect.md)

`statement`

SQL запит. Запит не може містити маркер параметрів.

`options`

Асоціативний масив, що містить параметри оператора. Параметр можна використовувати для запиту курсору, що прокручується, на серверах баз даних, що підтримують цю функцію.

Опис допустимих опцій оператора дивіться у розділі [db2setoption()](function.db2-set-option.md)

### Значення, що повертаються

Повертає ресурс оператора, у разі успішного виконання SQL-запиту або **`false`**, якщо базі даних не вдалося виконати SQL-запит.

### Приклади

**Приклад #1 Створення таблиці за допомогою **db2exec()****

У наступному прикладі **db2exec()** використовується для виконання набору DDL-запитів у процесі створення таблиці.

```php
<?php
$conn = db2_connect($database, $user, $password);

// Создание таблицы test
$create = 'CREATE TABLE animals (id INTEGER, breed VARCHAR(32),
    name CHAR(16), weight DECIMAL(7,2))';
$result = db2_exec($conn, $create);
if ($result) {
    print "Таблица создана.\n";
}

// Наполнение таблицы test
$animals = array(
    array(0, 'cat', 'Pook', 3.2),
    array(1, 'dog', 'Peaches', 12.3),
    array(2, 'horse', 'Smarty', 350.0),
    array(3, 'gold fish', 'Bubbles', 0.1),
    array(4, 'budgerigar', 'Gizmo', 0.2),
    array(5, 'goat', 'Rickety Ride', 9.7),
    array(6, 'llama', 'Sweater', 150)
);

foreach ($animals as $animal) {
    $rc = db2_exec($conn, "INSERT INTO animals (id, breed, name, weight)
      VALUES ({$animal[0]}, '{$animal[1]}', '{$animal[2]}', {$animal[3]})");
    if ($rc) {
        print "Добавлена запись... ";
    }
}
?>
```

Результат виконання цього прикладу:

```
Таблица создана.
Добавлена запись... Добавлена запись... Добавлена запись... Добавлена запись... Добавлена запись... Добавлена запись... Добавлена запись...
```

**Приклад #2 Виконання запиту SELECT з курсором, що прокручується.**

У наступному прикладі показано, як запросити курсор, що прокручується, для SQL-запиту, отриманого за допомогою **db2exec()**

```php
<?php
$conn = db2_connect($database, $user, $password);
$sql = "SELECT name FROM animals
    WHERE weight < 10.0
    ORDER BY name";
if ($conn) {
    require_once('prepare.inc');
    $stmt = db2_exec($conn, $sql, array('cursor' => DB2_SCROLLABLE));
    while ($row = db2_fetch_array($stmt)) {
        print "$row[0]\n";
    }
}
?>
```

Результат виконання цього прикладу:

```
Bubbles
Gizmo
Pook
Rickety Ride
```

**Приклад #3 Отримання даних XML як SQL ResultSet**

У цьому прикладі показано, як працювати з документами, що зберігаються в стовпці XML за допомогою бази даних SAMPLE. Використовуючи досить простий SQL/XML, цей приклад повертає деякі вузли в XML-документі у форматі SQL ResultSet, з яким знайома більшість користувачів.

```php
<?php

$conn = db2_connect("SAMPLE", "db2inst1", "ibmdb2");

$query = 'SELECT * FROM XMLTABLE(
    XMLNAMESPACES (DEFAULT \'http://posample.org\'),
    \'db2-fn:xmlcolumn("CUSTOMER.INFO")/customerinfo\'
    COLUMNS
    "CID" VARCHAR (50) PATH \'@Cid\',
    "NAME" VARCHAR (50) PATH \'name\',
    "PHONE" VARCHAR (50) PATH \'phone [ @type = "work"]\'
    ) AS T
    WHERE NAME = \'Kathy Smith\'
    ';
$stmt = db2_exec($conn, $query);

while($row = db2_fetch_object($stmt)){
    printf("$row->CID     $row->NAME     $row->PHONE\n");
}
db2_close($conn);

?>
```

Результат виконання цього прикладу:

```
1000     Kathy Smith     416-555-1358
1001     Kathy Smith     905-555-7258
```

**Приклад #4 Виконання "JOIN" з даними XML**

Наступний приклад працює з документами, що зберігаються у 2 різних стовпцях XML у базі даних SAMPLE. Він створює 2 тимчасові таблиці з XML-документів із 2 різних стовпців і повертає SQL ResultSet з інформацією про статус доставки для клієнта.

```php
<?php

$conn = db2_connect("SAMPLE", "db2inst1", "ibmdb2");

$query = '
    SELECT A.CID, A.NAME, A.PHONE, C.PONUM, C.STATUS
    FROM
    XMLTABLE(
    XMLNAMESPACES (DEFAULT \'http://posample.org\'),
    \'db2-fn:xmlcolumn("CUSTOMER.INFO")/customerinfo\'
    COLUMNS
    "CID" BIGINT PATH \'@Cid\',
    "NAME" VARCHAR (50) PATH \'name\',
    "PHONE" VARCHAR (50) PATH \'phone [ @type = "work"]\'
    ) as A,
    PURCHASEORDER AS B,
    XMLTABLE (
    XMLNAMESPACES (DEFAULT \'http://posample.org\'),
    \'db2-fn:xmlcolumn("PURCHASEORDER.PORDER")/PurchaseOrder\'
    COLUMNS
    "PONUM"  BIGINT PATH \'@PoNum\',
    "STATUS" VARCHAR (50) PATH \'@Status\'
    ) as C
    WHERE A.CID = B.CUSTID AND
    B.POID = C.PONUM AND
    A.NAME = \'Kathy Smith\'
';

$stmt = db2_exec($conn, $query);

while($row = db2_fetch_object($stmt)){
    printf("$row->CID     $row->NAME     $row->PHONE     $row->PONUM     $row->STATUS\n");
}

db2_close($conn);

?>
```

Результат виконання цього прикладу:

```
1001     Kathy Smith     905-555-7258     5002     Shipped
```

**Приклад #5 Повернення SQL-даних як частини великого XML-документа**

Наступний приклад працює з частиною документів PRODUCT.DESCRIPTION у базі даних SAMPLE. Він створює XML-документ, що містить опис продукту (дані XML) та інформацію про ціни (дані SQL).

```php
<?php

$conn = db2_connect("SAMPLE", "db2inst1", "ibmdb2");

$query = '
SELECT
XMLSERIALIZE(
XMLQUERY(\'
    declare boundary-space strip;
    declare default element namespace "http://posample.org";
    <promoList> {
    for $prod in $doc/product
    where $prod/description/price < 10.00
    order by $prod/description/price ascending
    return(
        <promoitem> {
        $prod,
        <startdate> {$start} </startdate>,
        <enddate> {$end} </enddate>,
        <promoprice> {$promo} </promoprice>
        } </promoitem>
    )
    } </promoList>
\' passing by ref DESCRIPTION AS "doc",
PROMOSTART as "start",
PROMOEND as "end",
PROMOPRICE as "promo"
RETURNING SEQUENCE)
AS CLOB (32000))
AS NEW_PRODUCT_INFO
FROM PRODUCT
WHERE PID = \'100-100-01\'
';

$stmt = db2_exec($conn, $query);

while($row = db2_fetch_array($stmt)){
    printf("$row[0]\n");
}
db2_close($conn);

?>
```

Результат виконання цього прикладу:

```
<promoList xmlns="http://posample.org">
    <promoitem>
    <product pid="100-100-01">
        <description>
            <name>Snow Shovel, Basic 22 inch</name>
            <details>Basic Snow Shovel, 22 inches wide, straight handle with D-Grip</details>
            <price>9.99</price>
            <weight>1 kg</weight>
        </description>
    </product>
    <startdate>2004-11-19</startdate>
    <enddate>2004-12-19</enddate>
    <promoprice>7.25</promoprice>
    </promoitem>
</promoList>
```

### Дивіться також

-   [db2execute()](function.db2-execute.md) - Виконує підготовлений SQL-запит
-   [db2prepare()](function.db2-prepare.md) - готує SQL-запит до виконання
