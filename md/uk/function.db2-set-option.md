---
navigation:
  - function.db2-server-info.md: « db2\_server\_info
  - function.db2-special-columns.md: db2\_special\_columns »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_set\_option
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_set\_option

(PECL ibm\_db2 >= 1.0.0)

db2\_set\_option — Встановіть опцію для з'єднання або ресурсу оператора.

### Опис

```methodsynopsis
db2_set_option(resource $resource, array $options, int $type): bool
```

Встановіть опцію для з'єднання або ресурсу оператора. Для ресурсу результуючого набору опції не можна задавати.

### Список параметрів

`resource`

Коректний ресурс оператора, отриманий з [db2\_prepare()](function.db2-prepare.md) або ж ресурс з'єднання, отриманий з [db2\_connect()](function.db2-connect.md) або [db2\_pconnect()](function.db2-pconnect.md)

`options`

Асоціативний масив, що містить опції, що відповідають ресурсу. Цей параметр можна використовувати для зміни режиму автопідтвердження транзакцій, типу курсору та завдання регістра імен стовпців (нижній, верхній, як є) у результуючому наборі.

`autocommit`

`DB2_AUTOCOMMIT_ON`\- включить режим автоподтверждения транзакций для заданного соединения.

`DB2_AUTOCOMMIT_OFF`\- отключить режим автоподтверждения транзакций для заданного соединения.

`cursor`

`DB2_FORWARD_ONLY` - Задати тип курсору "тільки вперед". Це тип за промовчанням і він підтримується всіма базами даних.

`DB2_SCROLLABLE` - задати тип курсору як "перемотується". Даний тип курсору дозволяє отримувати доступ до довільних рядків результуючого набору та доступний лише для IBM DB2 Universal Database.

`binmode`

`DB2_BINARY` - Визначає, що бінарні дані будуть повернуті як є. Це режим за промовчанням, він рівносильний завданню `ibm_db2.binmode=1`в php.ini.

`DB2_CONVERT` - Визначає, що бінарні дані будуть сконвертовані в шістнадцяткове подання. Рівносильно завдання `ibm_db2.binmode=2`в php.ini.

`DB2_CONVERT` - визначає, що бінарні дані будуть сконвертовані в **`null`**. Рівносильно завдання `ibm_db2.binmode=3`в php.ini.

`db2_attr_case`

`DB2_CASE_LOWER` - Визначає, що імена стовпців будуть повернуті в нижньому регістрі.

`DB2_CASE_UPPER` - Визначає, що імена стовпців будуть повернуті у верхньому регістрі.

`DB2_CASE_NATURAL` - Визначає, що імена стовпців будуть повернуті як є.

`deferred_prepare`

`DB2_DEFERRED_PREPARE_ON` - Включає відкладену підготовку ресурсу оператора.

`DB2_DEFERRED_PREPARE_OFF` - Вимикає відстрочену підготовку ресурсу оператора.

Наступні нові опції i5/OS доступні в ibm\_db2 версії 1.5.1 та вище. Ці опції доступні лише якщо PHP та ibm\_db2 запущено на системі i5.

`i5_fetch_only`

`DB2_I5_FETCH_ON` - курсори можуть бути тільки для читання і не можуть використовуватися для позиціонування DELETE або UPDATE. Є поведінкою за умовчанням, тільки якщо змінна оточення `SQL_ATTR_FOR_FETCH_ONLY`не установлена в`SQL_FALSE`

`DB2_I5_FETCH_OFF` - курсори можна використовувати для позиціонування DELETE або UPDATE.

Наступні нові опції доступні в ibm\_db2 версії 1.8.0 та вище.

`rowcount`

`DB2_ROWCOUNT_PREFETCH_ON` - клієнт може запитати кількість рядків перед вилученням, що означає, що функція [db2\_num\_rows()](function.db2-num-rows.md) поверне кількість вибраних рядків, навіть якщо використовується курсор `ROLLFORWARD_ONLY`

`DB2_ROWCOUNT_PREFETCH_OFF` - клієнт не може запитати кількість рядків перед вилученням

Наступні нові опції доступні в ibm\_db2 версії 1.7.0 та вище.

`trusted_user`

Щоб перевести користувача до статусу довіреного користувача, вкажіть ідентифікатор (рядок) довіреного користувача як значення цього параметра. Ця опція може бути задана лише ресурсу з'єднання. Для використання цієї опції необхідно, щоб з'єднання було дозволено довірений контекст.

`trusted_password`

Пароль (рядок), що відповідає ідентифікатору користувача, заданому в trusted\_user.

Наступні нові опції доступні в ibm\_db2 версії 1.6.0 та вище. Ці опції надають корисну інформацію, яку можна отримати через [db2\_get\_option()](function.db2-get-option.md)

> **Зауваження** :
> 
> Якщо значення кожної опції встановлено, деякі сервери можуть не зуміти обробити всі значення та обріжуть його.
> 
> Для впевненості в тому, що всі опції конвертовані коректно під час передачі на хост, використовуйте лише символи A-Z, 0-9, підкреслення(\_) та точку (.).

`userid`

`SQL_ATTR_INFO_USERID` - покажчик на символьний рядок, що закінчується null-байтом і містить ідентифікатор користувача, переданий базі при з'єднанні.

> **Зауваження** :
> 
> DB2 для серверів z/OS та OS/390 підтримує довжину до 16 символів. Ідентифікатор користувача не скомпрометує ідентифікатор авторизації – це різні сутності.

`acctstr`

`SQL_ATTR_INFO_ACCTSTR` - покажчик на символьний рядок, що закінчується null-байтом і використовується для ідентифікації облікового рядка клієнта, відповідного надісланого сервера при з'єднанні.

> **Зауваження** :
> 
> DB2 для серверів z/OS та OS/390 підтримує довжину до 200 символів.

`applname`

`SQL_ATTR_INFO_APPLNAME` - вказівник на символьний рядок, що закінчується null-байтом і використовується для ідентифікації імені клієнтської програми, відповідної надісланої на сервер під час з'єднання.

> **Зауваження** :
> 
> DB2 для серверів z/OS та OS/390 підтримує довжину до 32 символів.

`wrkstnname`

`SQL_ATTR_INFO_WRKSTNNAME` - вказівник на символьний рядок, що закінчується null-байтом і використовується для ідентифікації імені робочої станції, відповідної надісланої на сервер при з'єднанні.

> **Зауваження** :
> 
> DB2 для серверів z/OS та OS/390 підтримує довжину до 18 символів.

`type`

Цілочисленне значення, що визначає тип ресурсу, який було передано у функцію.

\- передан ресурс соединения.

Любое другое значение, отличное от означає ресурс оператора.

Наступна таблиця показує, які параметри сумісні з ресурсами:

**Матриця ресурс/параметр**

| Ключ | Значение | Тип ресурса |
| --- | --- | --- |
|  |  | З'єднання |
| autocommit | `DB2_AUTOCOMMIT_ON` | X |
| autocommit | `DB2_AUTOCOMMIT_OFF` | X |
| cursor | `DB2_SCROLLABLE` | \- |
| cursor | `DB2_FORWARD_ONLY` | \- |
| binmode | `DB2_BINARY` | X |
| binmode | `DB2_CONVERT` | X |
| binmode | `DB2_PASSTHRU` | X |
| db2\_attr\_case | `DB2_CASE_LOWER` | X |
| db2\_attr\_case | `DB2_CASE_UPPER` | X |
| db2\_attr\_case | `DB2_CASE_NATURAL` | X |
| deferred\_prepare | `DB2_DEFERRED_PREPARE_ON` | \- |
| deferred\_prepare | `DB2_DEFERRED_PREPARE_OFF` | \- |
| i5\_fetch\_only | `DB2_I5_FETCH_ON` | \- |
| i5\_fetch\_only | `DB2_I5_FETCH_OFF` | \- |
| rowcount | `DB2_ROWCOUNT_PREFETCH_ON` | \- |
| rowcount | `DB2_ROWCOUNT_PREFETCH_OFF` | \- |
| trusted\_user | `<USER NAME> (String)` | X |
| trusted\_password | `<PASSWORD> (String)` | X |
| userid | `SQL_ATTR_INFO_USERID` | X |
| acctstr | `SQL_ATTR_INFO_ACCTSTR` | X |
| applname | `SQL_ATTR_INFO_APPLNAME` | X |
| wrkstnname | `SQL_ATTR_INFO_WRKSTNNAME` | X |

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Встановлення одного параметра для ресурсу з'єднання**

```php
<?php
/* Параметры соединения с базой данных */
$database = 'SAMPLE';
$hostname = 'localhost';
$port = 50000;
$protocol = 'TCPIP';
$username = 'db2inst1';
$password = 'ibmdb2';

/* Строка соединения */
$conn_string = "DRIVER={IBM DB2 ODBC DRIVER};DATABASE=$database;";
$conn_string .= "HOSTNAME=$hostname;PORT=$port;PROTOCOL=$protocol;";
$conn_string .= "UID=$username;PWD=$password;";

/* Получаем ресурс соединения */
$conn = db2_connect($conn_string, '', '');

/* Создаём ассоциативный массив опций */
$options = array('autocommit' => DB2_AUTOCOMMIT_ON);

/* Вызываем функцию */
$result = db2_set_option($conn, $options, 1);

/* Проверяем, все ли опции установились */
if($result)
{
  echo 'Options Set Successfully';
}
else
{
  echo 'Could Not Set Options';
}
?>
```

Результат виконання наведеного прикладу:

```
Options Set Successfully
```

**Приклад #2 Встановлення кількох параметрів для ресурсу з'єднання**

```php
<?php
/* Параметры соединения с базой данных */
$database = 'SAMPLE';
$hostname = 'localhost';
$port = 50000;
$protocol = 'TCPIP';
$username = 'db2inst1';
$password = 'ibmdb2';

/* Строка соединения */
$conn_string = "DRIVER={IBM DB2 ODBC DRIVER};DATABASE=$database;";
$conn_string .= "HOSTNAME=$hostname;PORT=$port;PROTOCOL=$protocol;";
$conn_string .= "UID=$username;PWD=$password;";

/* Получаем ресурс соединения */
$conn = db2_connect($conn_string, '', '');

/* Создаём ассоциативный массив опций */
$options = array('autocommit' => DB2_AUTOCOMMIT_OFF,
                    'binmode' => DB2_PASSTHRU,
              'db2_attr_case' => DB2_CASE_UPPER,
                     'cursor' => DB2_SCROLLABLE);

/* Вызываем функцию */
$result = db2_set_option($conn, $options, 1);

/* Проверяем, все ли опции установились */
if($result)
{
  echo 'Options Set Successfully';
}
else
{
  echo 'Could Not Set Options';
}
?>
```

Результат виконання наведеного прикладу:

```
Options Set Successfully
```

**Приклад #3 Встановлення кількох параметрів з одним неправильним ключем**

```php
<?php
/* Параметры соединения с базой данных */
$database = 'SAMPLE';
$hostname = 'localhost';
$port = 50000;
$protocol = 'TCPIP';
$username = 'db2inst1';
$password = 'ibmdb2';

/* Строка соединения */
$conn_string = "DRIVER={IBM DB2 ODBC DRIVER};DATABASE=$database;";
$conn_string .= "HOSTNAME=$hostname;PORT=$port;PROTOCOL=$protocol;";
$conn_string .= "UID=$username;PWD=$password;";

/* Получаем ресурс соединения */
$conn = db2_connect($conn_string, '', '');

/* Создаём ассоциативный массив опций */
$options = array('autocommit' => DB2_AUTOCOMMIT_OFF,
             'MY_INVALID_KEY' => DB2_PASSTHRU,
              'db2_attr_case' => DB2_CASE_UPPER,
                     'cursor' => DB2_SCROLLABLE);

/* Вызываем функцию */
$result = db2_set_option($conn, $options, 1);

/* Проверяем, все ли опции установились */
if($result)
{
  echo 'Options Set Successfully';
}
else
{
  echo 'Could Not Set Options';
}
?>
```

Результат виконання наведеного прикладу:

```
Could Not Set Options
```

**Приклад #4 Встановлення кількох параметрів з одним неправильним значенням**

```php
<?php
/* Параметры соединения с базой данных */
$database = 'SAMPLE';
$hostname = 'localhost';
$port = 50000;
$protocol = 'TCPIP';
$username = 'db2inst1';
$password = 'ibmdb2';

/* Строка соединения */
$conn_string = "DRIVER={IBM DB2 ODBC DRIVER};DATABASE=$database;";
$conn_string .= "HOSTNAME=$hostname;PORT=$port;PROTOCOL=$protocol;";
$conn_string .= "UID=$username;PWD=$password;";

/* Получаем ресурс соединения */
$conn = db2_connect($conn_string, '', '');

/* Создаём ассоциативный массив опций */
$options = array('autocommit' => DB2_AUTOCOMMIT_OFF,
                    'binmode' => 'INVALID_VALUE',
              'db2_attr_case' => DB2_CASE_UPPER,
                     'cursor' => DB2_SCROLLABLE);

/* Вызываем функцию */
$result = db2_set_option($conn, $options, 1);

/* Проверяем, все ли опции установились */
if($result)
{
  echo 'Options Set Successfully';
}
else
{
  echo 'Could Not Set Options';
}
?>
```

Результат виконання наведеного прикладу:

```
Could Not Set Options
```

**Приклад #5 Setting multiple parameters with connection resource and the wrong type**

```php
<?php
/* Параметры соединения с базой данных */
$database = 'SAMPLE';
$hostname = 'localhost';
$port = 50000;
$protocol = 'TCPIP';
$username = 'db2inst1';
$password = 'ibmdb2';

/* Строка соединения */
$conn_string = "DRIVER={IBM DB2 ODBC DRIVER};DATABASE=$database;";
$conn_string .= "HOSTNAME=$hostname;PORT=$port;PROTOCOL=$protocol;";
$conn_string .= "UID=$username;PWD=$password;";

/* Получаем ресурс соединения */
$conn = db2_connect($conn_string, '', '');

/* Создаём ассоциативный массив опций */
$options = array('autocommit' => DB2_AUTOCOMMIT_OFF,
                    'binmode' => DB2_PASSTHRU,
              'db2_attr_case' => DB2_CASE_UPPER,
                     'cursor' => DB2_SCROLLABLE);

/* Вызываем функцию */
$result = db2_set_option($conn, $options, 2);

/* Проверяем, все ли опции установились */
if($result)
{
  echo 'Options Set Successfully';
}
else
{
  echo 'Could Not Set Options';
}
?>
```

Результат виконання наведеного прикладу:

```
Could Not Set Options
```

**Приклад #6 Setting multiple parameters with the wrong resource**

```php
<?php
/* Параметры соединения с базой данных */
$database = 'SAMPLE';
$hostname = 'localhost';
$port = 50000;
$protocol = 'TCPIP';
$username = 'db2inst1';
$password = 'ibmdb2';

/* Строка соединения */
$conn_string = "DRIVER={IBM DB2 ODBC DRIVER};DATABASE=$database;";
$conn_string .= "HOSTNAME=$hostname;PORT=$port;PROTOCOL=$protocol;";
$conn_string .= "UID=$username;PWD=$password;";

/* Получаем ресурс соединения */
$conn = db2_connect($conn_string, '', '');

/* Создаём ассоциативный массив опций */
$options = array('autocommit' => DB2_AUTOCOMMIT_OFF,
                    'binmode' => DB2_PASSTHRU,
              'db2_attr_case' => DB2_CASE_UPPER,
                     'cursor' => DB2_SCROLLABLE);

$stmt = db2_prepare($conn, 'SELECT * FROM EMPLOYEE');

/* Вызываем функцию */
$result = db2_set_option($stmt, $options, 1);

/* Проверяем, все ли опции установились */
if($result)
{
  echo 'Options Set Successfully';
}
else
{
  echo 'Could Not Set Options';
}
?>
```

Результат виконання наведеного прикладу:

```
Could Not Set Options
```

**Приклад #7 Putting it all together**

```php
<?php
/* Параметры соединения с базой данных */
$database = 'SAMPLE';
$hostname = 'localhost';
$port = 50000;
$protocol = 'TCPIP';
$username = 'db2inst1';
$password = 'ibmdb2';

/* Строка соединения */
$conn_string = "DRIVER={IBM DB2 ODBC DRIVER};DATABASE=$database;";
$conn_string .= "HOSTNAME=$hostname;PORT=$port;PROTOCOL=$protocol;";
$conn_string .= "UID=$username;PWD=$password;";

/* Получаем ресурс соединения */
$conn = db2_connect($conn_string, '', '');

/* Создаём ассоциативный массив опций */
$options = array('db2_attr_case' => DB2_CASE_LOWER,
                        'cursor' => DB2_SCROLLABLE);

$stmt = db2_prepare($conn, 'SELECT * FROM EMPLOYEE WHERE EMPNO = ? OR EMPNO = ?');

/* Вызываем функцию */
$option_result = db2_set_option($stmt, $options, 2);
$result = db2_execute($stmt, array('000130', '000140'));

/* Получаем строку 2 перед строкой 1. Перематываемый курсор! */
print_r(db2_fetch_assoc($stmt, 2));
print '<br /><br />';
print_r(db2_fetch_assoc($stmt, 1));

?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [empno] => 000140
    [firstnme] => HEATHER
    [midinit] => A
    [lastname] => NICHOLLS
    [workdept] => C01
    [phoneno] => 1793
    [hiredate] => 1976-12-15
    [job] => ANALYST
    [edlevel] => 18
    [sex] => F
    [birthdate] => 1946-01-19
    [salary] => 28420.00
    [bonus] => 600.00
    [comm] => 2274.00
)

Array
(
    [empno] => 000130
    [firstnme] => DELORES
    [midinit] => M
    [lastname] => QUINTANA
    [workdept] => C01
    [phoneno] => 4578
    [hiredate] => 1971-07-28
    [job] => ANALYST
    [edlevel] => 16
    [sex] => F
    [birthdate] => 1925-09-15
    [salary] => 23800.00
    [bonus] => 500.00
    [comm] => 1904.00
)
```

**Приклад #8 Курсор i5/OS тільки для читання**

```php
<?php
  $conn = db2_connect("", "", "", array("i5_lib"=>"nobody"));
  $stmt = db2_prepare($conn, 'select * from names where first = ?');
  $name = "first2";
  db2_bind_param($stmt, 1, "name", DB2_PARAM_IN);
  $options = array("i5_fetch_only"=>DB2_I5_FETCH_ON);
  db2_set_option($stmt,$options,0);
  if (db2_execute($stmt)) {
    while ($row = db2_fetch_array($stmt)) {
      echo "{$row[0]} {$row[1]}";
    }
  }
?>
```

Результат виконання наведеного прикладу:

```
first2 last2
```

### Дивіться також

-   [db2\_connect()](function.db2-connect.md) \- Повертає з'єднання з базою даних
-   [db2\_pconnect()](function.db2-pconnect.md) \- Повертає постійне з'єднання з базою даних
-   [db2\_exec()](function.db2-exec.md) \- Виконує SQL-запит безпосередньо
-   [db2\_prepare()](function.db2-prepare.md) \- готує SQL-запит до виконання
-   [db2\_cursor\_type()](function.db2-cursor-type.md) \- Повертає тип курсору, який використовується у ресурсі оператора
