- [«odbc_longreadlen](function.odbc-longreadlen.md)
- [odbc_num_fields »](function.odbc-num-fields.md)

- [PHP Manual](index.md)
- [Функції ODBC](ref.uodbc.md)
- Перевіряє, чи є кілька результатів.

#odbc_next_result

(PHP 4 \>= 4.0.5, PHP 5, PHP 7, PHP 8)

odbc_next_result — Перевіряє, чи є кілька результатів.

### Опис

**odbc_next_result**(resource `$statement`): bool

Перевіряє, чи доступні інші результуючі набори, а також
доступ до наступного результуючого набору за допомогою
[odbc_fetch_array()](function.odbc-fetch-array.md),
[odbc_fetch_row()](function.odbc-fetch-row.md),
[odbc_result()](function.odbc-result.md) і т.д.

### Список параметрів

`statement`
Ідентифікатор результату.

### Значення, що повертаються

Повертає **`true`** якщо доступні інші результуючі набори,
**`false`** інакше.

### Приклади

**Приклад #1 Приклад використання **odbc_next_result()****

` <?php$r_Connection = odbc_connect($dsn, $username, $password);$s_SQL = <<<END_SQLSELECT 'A'SELECT 'B'SELECT 'C'END_SQL;$r_Results = odbc_exe ;$a_Row1 = odbc_fetch_array($r_Results);$a_Row2 = odbc_fetch_array($r_Results);echo "Вывод первого результирующего набора ";var_dump($a_Row1, $a_Row2);echo "Получение второго результирующего набора ";var_dump(odbc_next_result($r_Results ));$a_Row1 = odbc_fetch_array($r_Results);$a_Row2 = odbc_fetch_array($r_Results);echo "Вывод второго результирующего набора ";var_dump($a_Row1, $a_Row2);echo "Получение третьего результирующего набора ";var_dump(odbc_next_result( $r_Results));$a_Row1 = odbc_fetch_array($r_Results);$a_Row2 = odbc_fetch_array($r_Results);echo "Вывод третьего результирующего набора ";var_dump($a_Row1, $a_Row2);echo "Попытка получения четвёртого результирующего набора ";var_dump (odbc_next_result($r_Results));?> `

Результат виконання цього прикладу:

Виведення першого результуючого набору array(1) {
["A"]=>
string(1) "A"
}
bool(false)
Отримання другого результуючого набору bool(true)
Виведення другого результуючого набору array(1) {
["B"]=>
string(1) "B"
}
bool(false)
Отримання третього результуючого набору bool(true)
Виведення третього результуючого набору array(1) {
["C"]=>
string(1) "C"
}
bool(false)
Спроба одержання четвертого результуючого набору bool(false)
