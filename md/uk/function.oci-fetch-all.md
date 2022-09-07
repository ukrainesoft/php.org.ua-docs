---
navigation:
  - function.oci-execute.md: « ociexecute
  - function.oci-fetch-array.md: ocifetcharray »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функции
title: ocifetchall
---
# ocifetchall

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocifetchall — Вибирає всі рядки з результату запиту на двовимірний масив.

### Опис

```methodsynopsis
oci_fetch_all(    resource $statement,    array &$output,    int $offset = 0,    int $limit = -1,    int $flags = OCI_FETCHSTATEMENT_BY_COLUMN | OCI_ASSOC): int
```

Вибирає всі рядки з результату запиту двомірний масив. За промовчанням повертає всі рядки.

Ця функція може бути викликана лише один раз для кожного запиту запущеного за допомогою [ociexecute()](function.oci-execute.md)

### Список параметрів

`statement`

Коректний ідентифікатор виразу OCI8, отриманий з [ociparse()](function.oci-parse.md) та виконаний функцією [ociexecute()](function.oci-execute.md), або ідентифікатор виразу `REF CURSOR`

`output`

Змінна, що містить повернені рядки.

LOB стовпці повертаються як рядки, для яких підтримується Oracle перетворення.

Дивіться [ocifetcharray()](function.oci-fetch-array.md) для більш детальної інформації про те, як проводиться вибірка даних та типів.

`offset`

Число рядків, які необхідно виключити з вибірки. За замовчуванням дорівнює 0, вибірка повертається з наступного ряду.

`limit`

Число рядків, що повертаються. За замовчуванням дорівнює -1, що означає повернення всіх рядків, починаючи із зазначених у `offset` + 1 попередній рядок.

`flags`

Параметр `flags` містить структуру масиву відбиває необхідність використання асоціативних масивів.

**Структура масиву **ocifetchall()****

| Константа | Описание |
| --- | --- |
| **`OCI_FETCHSTATEMENT_BY_ROW`** | Масив буде містити по одному підмасиву на кожен рядок запиту. |
| **`OCI_FETCHSTATEMENT_BY_COLUMN`** | Масив міститиме по одному підмасиву на кожен стовпець. Використовується за промовчанням. |

Масиви можуть бути проіндексовані або заголовками стовпців або пронумеровані. Повернеться лише один режим індексації.

**Індексація масиву **ocifetchall()****

| Константа | Описание |
| --- | --- |
| **`OCI_NUM`** | Для масиву кожного стовпця використовуються числові індекси. |
| **`OCI_ASSOC`** | Для масиву кожного стовпця використовують асоціативні індекси. За замовчуванням. |

Використовуйте оператор додавання "+" для вибору певної комбінації структури та індексації масиву.

Регістронезалежні (за замовчуванням у Oracle) імена полів у результуючому масиві матимуть асоціативні індекси у верхньому регістрі. Регістрозалежні імена полів матимуть індекси з тими самими регістрами символів, як і саме поле. Використовуйте [vardump()](function.var-dump.md) на `output`, щоб перевірити відповідність регістрів символів для кожного запиту.

У запитах, у яких є кілька стовпців з однаковими іменами, необхідно використовувати псевдоніми. Інакше лише один із стовпців з'явиться в асоціативному масиві.

### Значення, що повертаються

Повертає кількість стовпців у `output`, який може набувати значення 0 або більше.

### Приклади

**Приклад #1 Приклад використання **ocifetchall()****

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT POSTAL_CODE, CITY FROM locations WHERE ROWNUM < 3');
oci_execute($stid);

$nrows = oci_fetch_all($stid, $res);

echo "$nrows строк получено<br>\n";
var_dump($res);

// Вывод var_dump:
//    2 строк получено
//    array(2) {
//      ["POSTAL_CODE"]=>
//      array(2) {
//        [0]=>
//        string(6) "00989x"
//        [1]=>
//        string(6) "10934x"
//      }
//      ["CITY"]=>
//      array(2) {
//        [0]=>
//        string(4) "Roma"
//        [1]=>
//        string(6) "Venice"
//      }
//    }

// Форматирование результатов
echo "<table border='1'>\n";
foreach ($res as $col) {
    echo "<tr>\n";
    foreach ($col as $item) {
        echo "    <td>".($item !== null ? htmlentities($item, ENT_QUOTES) : "")."</td>\n";
    }
    echo "</tr>\n";
}
echo "</table>\n";

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #2 Приклад використання **ocifetchall()** з **`OCI_FETCHSTATEMENT_BY_ROW`****

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT POSTAL_CODE, CITY FROM locations WHERE ROWNUM < 3');
oci_execute($stid);

$nrows = oci_fetch_all($stid, $res, null, null, OCI_FETCHSTATEMENT_BY_ROW);

echo "$nrows строк получено<br>\n";
var_dump($res);

// Выведет:
//    2 строк получено
//    array(2) {
//      [0]=>
//      array(2) {
//        ["POSTAL_CODE"]=>
//        string(6) "00989x"
//        ["CITY"]=>
//        string(4) "Roma"
//      }
//      [1]=>
//      array(2) {
//        ["POSTAL_CODE"]=>
//        string(6) "10934x"
//        ["CITY"]=>
//        string(6) "Venice"
//      }
//    }

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #3 Приклад використання **ocifetchall()** з **`OCI_NUM`****

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT POSTAL_CODE, CITY FROM locations WHERE ROWNUM < 3');
oci_execute($stid);

$nrows = oci_fetch_all($stid, $res, null, null, OCI_FETCHSTATEMENT_BY_ROW + OCI_NUM);

echo "$nrows строк получено<br>\n";
var_dump($res);

// Выведет:
//    2 строк получено
//    array(2) {
//      [0]=>
//      array(2) {
//        [0]=>
//        string(6) "00989x"
//        [1]=>
//        string(4) "Roma"
//      }
//      [1]=>
//      array(2) {
//        [0]=>
//        string(6) "10934x"
//        [1]=>
//        string(6) "Venice"
//      }
//    }

oci_free_statement($stid);
oci_close($conn);

?>
```

### Примітки

> **Зауваження**
> 
> Використання `offset` неефективно. Всі ряди, що пропускаються, включаються в результат запиту повертається базою даних до PHP. Після цього вони виключаються. Більш ефективно використовувати SQL для відступу та обмеження рядів у запиті. Дивіться [ocifetcharray()](function.oci-fetch-array.md) для прикладів.

> **Зауваження**
> 
> Запити, що повертають велику кількість рядів, можуть бути більш ефективними, якщо використовується однорядна функція вибірки, така як [ocifetcharray()](function.oci-fetch-array.md)

> **Зауваження**
> 
> Для запитів, що повертають велику кількість рядів, продуктивність може бути значно збільшена за допомогою збільшення значення опції [oci8.defaultprefetch](oci8.configuration.md#ini.oci8.default-prefetch) або використання [ocisetprefetch()](function.oci-set-prefetch.md)

> **Зауваження**
> 
> Не повертає ряди для неявних результуючих наборів у Oracle Database 12*з*. Використовуйте замість цієї функції функцію [ocifetcharray()](function.oci-fetch-array.md)

### Дивіться також

-   [ocifetch()](function.oci-fetch.md) - Вибирає наступний рядок із результату в буфер
-   [ocifetcharray()](function.oci-fetch-array.md) - Повертає наступний рядок із результату запиту у вигляді асоціативного чи нумерованого масиву
-   [ocifetchassoc()](function.oci-fetch-assoc.md) - Повертає наступний рядок із результату запиту у вигляді асоціативного масиву
-   [ocifetchobject()](function.oci-fetch-object.md) - Повертає наступний рядок із результату запиту у вигляді об'єкта
-   [ocifetchrow()](function.oci-fetch-row.md) - Повертає наступний рядок із результату запиту у вигляді нумерованого масиву
-   [ocisetprefetch()](function.oci-set-prefetch.md) - Встановлює кількість рядків, які будуть автоматично вибрані у буфер
