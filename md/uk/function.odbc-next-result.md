---
navigation:
  - function.odbc-longreadlen.md: « odbclongreadlen
  - function.odbc-num-fields.md: odbcnumfields »
  - index.md: PHP Manual
  - ref.uodbc.md: Функции ODBC
title: odbcnextresult
---
# odbcnextresult

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

odbcnextresult — Перевіряє, чи є кілька результатів.

### Опис

```methodsynopsis
odbc_next_result(resource $statement): bool
```

Перевіряє, чи доступні інші результуючі набори, а також дозволяє доступ до наступного результуючого набору за допомогою [odbcfetcharray()](function.odbc-fetch-array.md) [odbcfetchrow()](function.odbc-fetch-row.md) [odbcresult()](function.odbc-result.md) і т.д.

### Список параметрів

`statement`

Ідентифікатор результату.

### Значення, що повертаються

Повертає **`true`** якщо доступні інші результуючі набори, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **odbcnextresult()****

```php
<?php
$r_Connection = odbc_connect($dsn, $username, $password);

$s_SQL = <<<END_SQL
SELECT 'A'
SELECT 'B'
SELECT 'C'
END_SQL;

$r_Results = odbc_exec($r_Connection, $s_SQL);

$a_Row1 = odbc_fetch_array($r_Results);
$a_Row2 = odbc_fetch_array($r_Results);
echo "Вывод первого результирующего набора ";
var_dump($a_Row1, $a_Row2);

echo "Получение второго результирующего набора ";
var_dump(odbc_next_result($r_Results));

$a_Row1 = odbc_fetch_array($r_Results);
$a_Row2 = odbc_fetch_array($r_Results);
echo "Вывод второго результирующего набора ";
var_dump($a_Row1, $a_Row2);

echo "Получение третьего результирующего набора ";
var_dump(odbc_next_result($r_Results));

$a_Row1 = odbc_fetch_array($r_Results);
$a_Row2 = odbc_fetch_array($r_Results);
echo "Вывод третьего результирующего набора ";
var_dump($a_Row1, $a_Row2);

echo "Попытка получения четвёртого результирующего набора ";
var_dump(odbc_next_result($r_Results));
?>
```

Результат виконання цього прикладу:

```
Вывод первого результирующего набора array(1) {
  ["A"]=>
  string(1) "A"
}
bool(false)
Получение второго результирующего набора bool(true)
Вывод второго результирующего набора array(1) {
  ["B"]=>
  string(1) "B"
}
bool(false)
Получение третьего результирующего набора bool(true)
Вывод третьего результирующего набора array(1) {
  ["C"]=>
  string(1) "C"
}
bool(false)
Попытка получения четвёртого результирующего набора bool(false)
```
