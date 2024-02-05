---
navigation:
  - function.db2-exec.md: « db2\_exec
  - function.db2-fetch-array.md: db2\_fetch\_array »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_execute
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_execute

(PECL ibm\_db2 >= 1.0.0)

db2\_execute - Виконує підготовлений SQL-запит

### Опис

```methodsynopsis
db2_execute(resource $stmt, array $parameters = []): bool
```

**db2\_execute()** виконує SQL-запит, підготовлений за допомогою [db2\_prepare()](function.db2-prepare.md)

Якщо SQL-запит повертає набір результатів, наприклад, інструкція SELECT або CALL для процедури, що зберігається, яка повертає один або кілька наборів результатів, ви можете отримати рядок як масив з ресурсу `stmt`, используя[db2\_fetch\_assoc()](function.db2-fetch-assoc.md) [db2\_fetch\_both()](function.db2-fetch-both.md) або [db2\_fetch\_array()](function.db2-fetch-array.md). Як альтернативу ви можете використовувати [db2\_fetch\_row()](function.db2-fetch-row.md) для переміщення покажчика набору результатів на наступний рядок та вибірки стовпця з цього рядка за допомогою [db2\_result()](function.db2-result.md)

Обратитесь к[db2\_prepare()](function.db2-prepare.md)для краткого обсуждения преимуществ использования[db2\_prepare()](function.db2-prepare.md)и**db2\_execute()** замість [db2\_exec()](function.db2-exec.md)

### Список параметрів

`stmt`

Підготовлений запит, який повертається функцією [db2\_prepare()](function.db2-prepare.md)

`parameters`

Масив вхідних параметрів, які відповідають будь-яким маркерам параметрів, що містяться в підготовленому запиті.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Підготовка та виконання SQL-запиту з маркерами параметрів**

У наступному прикладі готується запит INSERT, який приймає чотири маркери параметрів, а потім виконує ітерацію масивів, що містять вхідні значення, які необхідно передати в **db2\_execute()**

```php
<?php
$pet = array(0, 'cat', 'Pook', 3.2);

$insert = 'INSERT INTO animals (id, breed, name, weight)
    VALUES (?, ?, ?, ?)';

$stmt = db2_prepare($conn, $insert);
if ($stmt) {
    $result = db2_execute($stmt, $pet);
    if ($result) {
        print "Успешно добавлен новый питомец.";
    }
}
?>
```

Результат виконання наведеного прикладу:

```
Успешно добавлен новый питомец.
```

**Приклад #2 Виклик збереженої процедури з параметром OUT**

У наступному прикладі готується запит CALL, який приймає один маркер параметра, що представляє параметр OUT, пов'язує змінну PHP `$my_pets`с параметром с помощью[db2\_bind\_param()](function.db2-bind-param.md), а потім викликає **db2\_execute()** для виконання запиту CALL. Після виконання запиту CALL процедури, що зберігається значення `$num_pets` змінюється, щоб відобразити значення, що повертається процедурою, що зберігається для цього параметра OUT.

```php
<?php
$num_pets = 0;
$res = db2_prepare($conn, "CALL count_my_pets(?)");
$rc = db2_bind_param($res, 1, "num_pets", DB2_PARAM_OUT);
$rc = db2_execute($res);
print "У меня $num_pets домашних животных!";
?>
```

Результат виконання наведеного прикладу:

```
У меня 7 домашних животных!
```

**Приклад #3 Повернення XML-даних як SQL ResultSet**

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
    WHERE NAME = ?
    ';

$stmt = db2_prepare($conn, $query);

$name = 'Kathy Smith';

if ($stmt) {
    db2_bind_param($stmt, 1, "name", DB2_PARAM_IN);
    db2_execute($stmt);

    while($row = db2_fetch_object($stmt)){
    printf("$row->CID     $row->NAME     $row->PHONE\n");
    }
}
db2_close($conn);

?>
```

Результат виконання наведеного прикладу:

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
    A.NAME = ?
';

$stmt = db2_prepare($conn, $query);

$name = 'Kathy Smith';

if ($stmt) {
    db2_bind_param($stmt, 1, "name", DB2_PARAM_IN);
    db2_execute($stmt);

    while($row = db2_fetch_object($stmt)){
    printf("$row->CID     $row->NAME     $row->PHONE     $row->PONUM     $row->STATUS\n");
    }
}

db2_close($conn);

?>
```

Результат виконання наведеного прикладу:

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
WHERE PID = ?
';

$stmt = db2_prepare($conn, $query);

$pid = "100-100-01";

if ($stmt) {
    db2_bind_param($stmt, 1, "pid", DB2_PARAM_IN);
    db2_execute($stmt);

    while($row = db2_fetch_array($stmt)){
    printf("$row[0]\n");
    }
}

db2_close($conn);

?>
```

Результат виконання наведеного прикладу:

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

-   [db2\_exec()](function.db2-exec.md) \- Виконує SQL-запит безпосередньо
-   [db2\_fetch\_array()](function.db2-fetch-array.md) \- Повертає масив, індексований за положенням стовпця, що представляє рядок у наборі результатів
-   [db2\_fetch\_assoc()](function.db2-fetch-assoc.md) \- Повертає масив, індексований на ім'я стовпця, що представляє рядок у наборі результатів
-   [db2\_fetch\_both()](function.db2-fetch-both.md) \- Повертає масив, індексований як на ім'я стовпця, так і за позицією, що представляє рядок у наборі результатів
-   [db2\_fetch\_row()](function.db2-fetch-row.md) \- Встановлює вказівник набору результатів на наступний рядок або запрошений рядок
-   [db2\_prepare()](function.db2-prepare.md) \- готує SQL-запит до виконання
-   [db2\_result()](function.db2-result.md) \- Повертає один стовпець з рядка у наборі результатів
