- [«db2_server_info](function.db2-server-info.md)
- [db2_special_columns »](function.db2-special-columns.md)

- [PHP Manual](index.md)
- [Функції IBM DB2](ref.ibm-db2.md)
- Встановлення опції для з'єднання чи ресурсу оператора

#db2_set_option

(PECL ibm_db2 \>= 1.0.0)

db2_set_option — Встановіть опцію для з'єднання або ресурсу оператора.

### Опис

**db2_set_option**(resource `$resource`, array `$options`, int `$type`):
bool

Встановіть опцію для з'єднання або ресурсу оператора. Для ресурсу
результуючого набору опції задавати не можна.

### Список параметрів

`resource`
Коректний ресурс оператора, отриманий з
[db2_prepare()](function.db2-prepare.md) або ресурс з'єднання,
отриманий з [db2_connect()](function.db2-connect.md) або
[db2_pconnect()](function.db2-pconnect.md).

`options`
Асоціативний масив, що містить опції, що відповідають ресурсу. Цей
параметр можна використовувати для зміни режиму автопідтвердження
транзакцій, типу курсору та завдання регістру імен стовпців (нижній,
верхній, як є) у результуючому наборі.

`autocommit`
`DB2_AUTOCOMMIT_ON` - включити режим автопідтвердження транзакцій для
заданого з'єднання.

`DB2_AUTOCOMMIT_OFF` - вимкнути режим автопідтвердження транзакцій для
заданого з'єднання.

`cursor`
`DB2_FORWARD_ONLY` - встановити тип курсору "тільки вперед". Це тип по
замовчуванням і він підтримується всіма базами даних.

`DB2_SCROLLABLE` - задати тип курсору як "перемотується". Цей тип
курсора дозволяє отримувати доступ до довільних рядків результуючого
доступний лише для IBM DB2 Universal Database.

`binmode`
`DB2_BINARY` - визначає, що бінарні дані будуть повернені як
є. Це режим за промовчанням, він рівнозначний завданням `ibm_db2.binmode=1`
в `php.ini`.

`DB2_CONVERT` - визначає, що бінарні дані будуть сконвертовані в
шістнадцяткове уявлення. Рівносильне завдання `ibm_db2.binmode=2`
в `php.ini`.

`DB2_CONVERT` - визначає, що бінарні дані будуть сконвертовані в
**`null`**. Рівносильно завдання `ibm_db2.binmode=3` в `php.ini`.

`db2_attr_case`
`DB2_CASE_LOWER` - визначає, що імена стовпців будуть повернуті до
нижньому регістрі.

DB2_CASE_UPPER - визначає, що імена стовпців будуть повернуті в
верхньому регістрі.

`DB2_CASE_NATURAL` - визначає, що імена стовпців будуть повернуті як
є.

`deferred_prepare`
`DB2_DEFERRED_PREPARE_ON` - включає відкладену підготовку ресурсу
оператора.

`DB2_DEFERRED_PREPARE_OFF` - вимикає відкладену підготовку ресурсу
оператора.

Наступні нові опції i5/OS доступні у ibm_db2 версії 1.5.1 та вище. Ці
опції доступні лише якщо PHP та ibm_db2 запущені на системі i5.

`i5_fetch_only`
DB2_I5_FETCH_ON - курсори можуть бути тільки для читання і не можуть
використовуватися для позиціонування DELETE або UPDATE. Є
поведінкою за умовчанням, тільки якщо змінна оточення
`SQL_ATTR_FOR_FETCH_ONLY` не встановлена в `SQL_FALSE`.

`DB2_I5_FETCH_OFF` - курсори можна використовувати для позиціонування при
DELETE чи UPDATE.

Наступні нові опції доступні в ibm_db2 версії 1.8.0 та вище.

`rowcount`
`DB2_ROWCOUNT_PREFETCH_ON` - клієнт може запросити кількість рядків
перед вилученням, що означає, що функція
[db2_num_rows()](function.db2-num-rows.md) поверне кількість
вибраних рядків, навіть якщо використовується курсор `ROLLFORWARD_ONLY`.

`DB2_ROWCOUNT_PREFETCH_OFF` - клієнт не може запросити кількість рядків
перед вилученням

Наступні нові опції доступні у ibm_db2 версії 1.7.0 та вище.

`trusted_user`
Щоб перевести користувача до статусу довіреного користувача, вкажіть
ідентифікатор (рядок) довіреного користувача як значення
цього параметра. Ця опція може бути задана лише для ресурсу
з'єднання. Для використання цієї опції необхідно, щоб
з'єднання було дозволено довірений контекст.

`trusted_password`
Пароль (рядок), який відповідає ідентифікатору користувача, заданому
у trusted_user.

Наступні нові опції доступні в ibm_db2 версії 1.6.0 та вище. Ці опції
надають корисну інформацію, яку можна отримати через
[db2_get_option()](function.db2-get-option.md).

> **Примітка**:
>
> Якщо значення кожної опції встановлено, деякі сервери можуть не зуміти
> обробити все значення і обріжуть його.
>
> Для впевненості в тому, що всі опції конвертовані коректно при
> передачі на хост, використовуйте лише символи A-Z, 0-9,
> підкреслення (\_) та точку (.).

`userid`
`SQL_ATTR_INFO_USERID` - покажчик на символьний рядок, що закінчується
null-байтом і містить ідентифікатор користувача, переданий базі
даний при з'єднанні.

> **Примітка**:
>
> DB2 для серверів z/OS та OS/390 підтримує довжину до 16
> символи. Ідентифікатор користувача не скомпрометує
> Ідентифікатор авторизації – це різні сутності.

`acctstr`
`SQL_ATTR_INFO_ACCTSTR` - покажчик на символьний рядок, що закінчується
null-байтом і використовується для ідентифікації облікового рядка клієнта,
відповідної надісланої на сервер при з'єднанні.

> **Примітка**:
>
> DB2 для серверів z/OS та OS/390 підтримує довжину аж до 200
> символи.

`applname`
`SQL_ATTR_INFO_APPLNAME` - вказівник на символьний рядок, що закінчується
null-байтом і використовується для ідентифікації клієнтського імені
програми, відповідної надісланої на сервер при з'єднанні.

> **Примітка**:
>
> DB2 для серверів z/OS та OS/390 підтримує довжину аж до 32
> символи.

`wrkstnname`
`SQL_ATTR_INFO_WRKSTNNAME` - вказівник на символьний рядок, що закінчується
null-байтом і використовується для ідентифікації імені робочої станції,
відповідної надісланої на сервер при з'єднанні.

> **Примітка**:
>
> DB2 для серверів z/OS та OS/390 підтримує довжину до 18
> символи.

`type`
Цілочисленне значення, що визначає тип ресурсу, який був переданий у
функцію.

`1` - переданий ресурс з'єднання.

Будь-яке інше значення, відмінне від `1` означає ресурс оператора.

Наступна таблиця показує, які параметри сумісні з якими
ресурсами:

| Ключ             | Значення                  | Тип ресурсу |          |                    |
| ---------------- | ------------------------- | ----------- | -------- | ------------------ |
|                  |                           | Поєднання   | Оператор | Результуючий набір |
| autocommit       | DB2_AUTOCOMMIT_ON         | X           | \-       | \-                 |             |          
| autocommit       | DB2_AUTOCOMMIT_OFF        | X           | \-       | \-                 |
| Cursor           | DB2_SCROLLABLE            | \-          | X        | \-                 |
| Cursor           | DB2_FORWARD_ONLY          | \-          | X        | \-                 |
| binmode          | DB2_BINARY                | X           | X        | \-                 |
| binmode          | DB2_CONVERT               | X           | X        | \-                 |
| binmode          | DB2_PASSTHRU              | X           | X        | \-                 |
| db2_attr_case    | DB2_CASE_LOWER            | X           | X        | \-                 |
| db2_attr_case    | DB2_CASE_UPPER            | X           | X        | \-                 |
| db2_attr_case    | DB2_CASE_NATURAL          | X           | X        | \-                 |
| deferred_prepare | DB2_DEFERRED_PREPARE_ON   | \-          | X        | \-                 |
| deferred_prepare | DB2_DEFERRED_PREPARE_OFF  | \-          | X        | \-                 |
| i5_fetch_only    | DB2_I5_FETCH_ON           | \-          | X        | \-                 |
| i5_fetch_only    | DB2_I5_FETCH_OFF          | \-          | X        | \-                 |
| rowcount         | DB2_ROWCOUNT_PREFETCH_ON  | \-          | X        | \-                 |
| rowcount         | DB2_ROWCOUNT_PREFETCH_OFF | \-          | X        | \-                 |
| trusted_user     | <USER NAME> (String)      | X           | \-       | \-                 |
| trusted_password | <PASSWORD> (String)       | X           | \-       | \-                 |
| userid           | SQL_ATTR_INFO_USERID      | X           | X        | \-                 |
| acctstr          | SQL_ATTR_INFO_ACCTSTR     | X           | X        | \-                 |
| applname         | SQL_ATTR_INFO_APPLNAME    | X           | X        | \-                 |
| wrkstnname       | SQL_ATTR_INFO_WRKSTNNAME  | X           | X        | \-                 |

**Матриця ресурс/параметр**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Встановлення одного параметра для ресурсу з'єднання**

` <?php/* Параметри з'єднання з базою даних */$database = 'SAMPLE';$hostname = 'localhost';$port = 50000;$protocol = 'TCPIP';$username =    ibmdb2';/* Рядок з'єднання */$conn_string = "DRIVER={IBM DB2 ODBC DRIVER};DATABASE=$database;";$conn_string .= "HOSTNAME=$hostname;PORT=$port;PROTOCOL= ;$conn_string .= "UID=$username;PWD=$password;";/* Отримуємо ресурс з'єднання */$conn = db2_connect($conn_string, '', '');/* Створюємо ассоциативный  = array('autocommit' => DB2_AUTOCOMMIT_ON);/* Викликаємо функцію */$result = db2_set_option($conn, $options, 1);/* Перевіряємо, всілі опції  Set Successfully';}else{ echo 'Could Not Set Options';}?> `

Результат виконання цього прикладу:

Options Set Successfully

**Приклад #2 Встановлення кількох параметрів для ресурсу з'єднання**

` <?php/* Параметри з'єднання з базою даних */$database = 'SAMPLE';$hostname = 'localhost';$port = 50000;$protocol = 'TCPIP';$username =    ibmdb2';/* Рядок з'єднання */$conn_string = "DRIVER={IBM DB2 ODBC DRIVER};DATABASE=$database;";$conn_string .= "HOSTNAME=$hostname;PORT=$port;PROTOCOL= ;$conn_string .= "UID=$username;PWD=$password;";/* Отримуємо ресурс з'єднання */$conn = db2_connect($conn_string, '', '');/* Створюємо ассоциативный  = array('autocommit' => DB2_AUTOCOMMIT_OFF,                    'binmode' => DB2_PASSTHRU,              'db2_attr_case' => DB2_CASE_UPPER,                     'cursor' => DB2_SCROLLABLE);/* Вызываем функцию */$result = db2_set_option($conn, $options, 1 );/* Перевіряємо, всі лі опції встановилися */if($result){ echo 'Options Set Successfully';}else{ echo 'Could Not Set Options';}?

Результат виконання цього прикладу:

Options Set Successfully

**Приклад #3 Встановлення кількох параметрів з одним некоректним
ключем**

` <?php/* Параметри з'єднання з базою даних */$database = 'SAMPLE';$hostname = 'localhost';$port = 50000;$protocol = 'TCPIP';$username =    ibmdb2';/* Рядок з'єднання */$conn_string = "DRIVER={IBM DB2 ODBC DRIVER};DATABASE=$database;";$conn_string .= "HOSTNAME=$hostname;PORT=$port;PROTOCOL= ;$conn_string .= "UID=$username;PWD=$password;";/* Отримуємо ресурс з'єднання */$conn = db2_connect($conn_string, '', '');/* Створюємо ассоциативный  = array('autocommit' => DB2_AUTOCOMMIT_OFF,             'MY_INVALID_KEY' => DB2_PASSTHRU,              'db2_attr_case' => DB2_CASE_UPPER,                     'cursor' => DB2_SCROLLABLE);/* Вызываем функцию */$result = db2_set_option($conn, $options, 1 );/* Перевіряємо, усі ли опції встановилися */if($result){ echo 'Options Set Successfully';}else{ echo 'Could Not Set Options';}> `

Результат виконання цього прикладу:

Could Not Set Options

**Приклад #4 Встановлення кількох параметрів з одним некоректним
значенням**

` <?php/* Параметри з'єднання з базою даних */$database = 'SAMPLE';$hostname = 'localhost';$port = 50000;$protocol = 'TCPIP';$username =    ibmdb2';/* Рядок з'єднання */$conn_string = "DRIVER={IBM DB2 ODBC DRIVER};DATABASE=$database;";$conn_string .= "HOSTNAME=$hostname;PORT=$port;PROTOCOL= ;$conn_string .= "UID=$username;PWD=$password;";/* Отримуємо ресурс з'єднання */$conn = db2_connect($conn_string, '', '');/* Створюємо ассоциативный  = array('autocommit' => DB2_AUTOCOMMIT_OFF,                    'binmode' => 'INVALID_VALUE',              'db2_attr_case' => DB2_CASE_UPPER,                     'cursor' => DB2_SCROLLABLE);/* Вызываем функцию */$result = db2_set_option($conn, $options , 1);/* Перевіряємо, всі лі опції встановилися */if($result){  echo 'Options Set Successfully';}else{ echo 'Could Not Set Options';

Результат виконання цього прикладу:

Could Not Set Options

**Приклад #5 Setting multiple parameters with a connection resource and
the wrong type**

` <?php/* Параметри з'єднання з базою даних */$database = 'SAMPLE';$hostname = 'localhost';$port = 50000;$protocol = 'TCPIP';$username =    ibmdb2';/* Рядок з'єднання */$conn_string = "DRIVER={IBM DB2 ODBC DRIVER};DATABASE=$database;";$conn_string .= "HOSTNAME=$hostname;PORT=$port;PROTOCOL= ;$conn_string .= "UID=$username;PWD=$password;";/* Отримуємо ресурс з'єднання */$conn = db2_connect($conn_string, '', '');/* Створюємо ассоциативный  = array('autocommit' => DB2_AUTOCOMMIT_OFF,                    'binmode' => DB2_PASSTHRU,              'db2_attr_case' => DB2_CASE_UPPER,                     'cursor' => DB2_SCROLLABLE);/* Вызываем функцию */$result = db2_set_option($conn, $options, 2 );/* Перевіряємо, усі ли опції встановилися */if($result){ echo 'Options Set Successfully';}else{ echo 'Could Not Set Options';}> `

Результат виконання цього прикладу:

Could Not Set Options

**Приклад #6 Setting multiple parameters with the wrong resource**

` <?php/* Параметри з'єднання з базою даних */$database = 'SAMPLE';$hostname = 'localhost';$port = 50000;$protocol = 'TCPIP';$username =    ibmdb2';/* Рядок з'єднання */$conn_string = "DRIVER={IBM DB2 ODBC DRIVER};DATABASE=$database;";$conn_string .= "HOSTNAME=$hostname;PORT=$port;PROTOCOL= ;$conn_string .= "UID=$username;PWD=$password;";/* Отримуємо ресурс з'єднання */$conn = db2_connect($conn_string, '', '');/* Створюємо ассоциативный  = array('autocommit' => DB2_AUTOCOMMIT_OFF,                    'binmode' => DB2_PASSTHRU,              'db2_attr_case' => DB2_CASE_UPPER,                     'cursor' => DB2_SCROLLABLE);$stmt = db2_prepare($conn, 'SELECT * FROM EMPLOYEE');/* Викликаємо функцію */$result = db2_set_option($stmt, $options, 1);/* Перевіряємо, всі лі опції встановилися */if($result){  echo 'Options Set S? ';}?> `

Результат виконання цього прикладу:

Could Not Set Options

**Приклад #7 Putting it all together**

` <?php/* Параметри з'єднання з базою даних */$database = 'SAMPLE';$hostname = 'localhost';$port = 50000;$protocol = 'TCPIP';$username =    ibmdb2';/* Рядок з'єднання */$conn_string = "DRIVER={IBM DB2 ODBC DRIVER};DATABASE=$database;";$conn_string .= "HOSTNAME=$hostname;PORT=$port;PROTOCOL= ;$conn_string .= "UID=$username;PWD=$password;";/* Отримуємо ресурс з'єднання */$conn = db2_connect($conn_string, '', '');/* Створюємо ассоциативный  = array('db2_attr_case' => DB2_CASE_LOWER,                        'cursor' => DB2_SCROLLABLE);$stmt = db2_prepare($conn, 'SELECT * FROM EMPLOYEE WHERE EMPNO = ? OR EMPNO = ?');/* Вызываем функцию */$option_result = db2_set_option($stmt, $options, 2);$result = db2_execute($stmt, array('000130', '000140'));/* Отримуємо рядок 2 перед рядком */print_r(db2_fetch_assoc($stmt, 2));print '<br /><br />';print_r(db2_fetch_assoc($stmt, 1));?> `

Результат виконання цього прикладу:

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

**Приклад #8 Курсор i5/OS тільки для читання**

` <?php  $conn = db2_connect("", "", "", array("i5_lib"=>"nobody")); $stmt = db2_prepare($conn, 'select * from names wherefirst = ?'); $name=="first2"; db2_bind_param($stmt, 1, "name", DB2_PARAM_IN); $options==array("i5_fetch_only"=>DB2_I5_FETCH_ON); db2_set_option($stmt,$options,0); if (db2_execute($stmt)) {    while ($row = db2_fetch_array($stmt)) {     echo "{$row[0]} {$row[1]}"; }  }?> `

Результат виконання цього прикладу:

first2 last2

### Дивіться також

- [db2_connect()](function.db2-connect.md) - Повертає з'єднання з
базою даних
- [db2_pconnect()](function.db2-pconnect.md) - Повертає постійне
з'єднання з базою даних
- [db2_exec()](function.db2-exec.md) - Виконує SQL-запит безпосередньо
- [db2_prepare()](function.db2-prepare.md) - Підготовка
SQL-запит до виконання
- [db2_cursor_type()](function.db2-cursor-type.md) - Повертає тип
курсор, який використовується в ресурсі оператора
