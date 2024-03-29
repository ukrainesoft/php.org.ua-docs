---
navigation:
  - function.oci-commit.md: « oci\_commit
  - function.oci-define-by-name.md: oci\_define\_by\_name »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_connect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_connect

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_connect — Встановлює з'єднання з базою даних Oracle

### Опис

```methodsynopsis
oci_connect(    string $username,    string $password,    ?string $connection_string = null,    string $encoding = "",    int $session_mode = OCI_DEFAULT): resource|false
```

Повертає ідентифікатор з'єднання, який використовується більшістю функцій модуля.

Для підвищення продуктивності більшість програм повинні використовувати постійні з'єднання за допомогою [oci\_pconnect()](function.oci-pconnect.md) замість \*\*oci\_connect()\*\*Смотрите[Управління з'єднанням](oci8.connection.md) для більш детальної інформації з управління з'єднаннями та створення пулів підключень.

Другий та наступні виклики функції **oci\_connect()** з тими ж параметрами повернуть ідентифікатор відкритого з'єднання. Це означає, що транзакції використовують *одне і теж* базове з'єднання із базою даних. При необхідності поділу транзакцій рекомендується використовувати функцію [oci\_new\_connect()](function.oci-new-connect.md)

### Список параметрів

`username`

Ім'я користувача Oracle.

`password`

Пароль`username`

`connection_string`

Містить `екземпляр Oracle` для підключення. Це може бути [» Easy Connect string](https://www.oracle.com/pls/topic/lookup?ctx=dblatest&id=GUID-E5358DEA-D619-4B7B-A799-3D2F802500F1), або Connect Name з файлу tnsnames.ora, або ім'я локального екземпляра Oracle.

Якщо не вказано окремо або **`null`**, PHP використовує змінні оточення, такі як **`TWO_TASK`**(на Linux) или\*\*`LOCAL`**(на Windows) и**`ORACLE_SID`\*\*для определения`екземпляра Oracle`для соединения.

Для використання методу Easy Connect, PHP має бути з'єднаний з клієнтськими бібліотеками версії Oracle 10*g*или старше. Easy Connect string для Oracle 10*g*принимает следующую форму:*\[//\]host\_name\[:port\]\[/service\_name\]*. Починаючи з Oracle 11*g* синтаксис такий: *\[//\]host\_name\[:port\]\[/service\_name\]\[:server\_type\]\[/instance\_name\]*. У Oracle 19c було введено додаткові параметри, включаючи налаштування часу очікування та перевірки активності. Зверніться до документації Oracle. Назви служб можуть бути визначені за допомогою запуску Oracle утиліти `lsnrctl status` на сервері бази даних.

Файл tnsnames.ora може знаходитись у пошуковому шляху Oracle Net, який включає /your/path/to/instantclient/network/admin, $ORACLE\_HOME/network/admin та /etc. Як альтернативний варіант можна встановити `TNS_ADMIN` таким чином, щоб шлях $TNS\_ADMIN/tnsnames.ora читав. Переконайтеся, що веб-сервер має доступ до файлу.

`encoding`

Визначає кодування, яке використовуватимуть клієнтські бібліотеки Oracle. Це кодування не обов'язково має збігатися з кодуванням, яке використовується в самій базі даних. Якщо вона не збігається, Oracle зробить все можливе для конвертування даних з-і в це кодування. Залежно від використовуваних кодувань, це може не завжди давати прийнятні результати. Перетворення також створює деякі додаткові витрати часу.

Якщо кодування не вказано, клієнтські бібліотеки Oracle будуть визначати його зі змінного оточення. **`NLS_LANG`**

Передача цього параметра може зменшити час, що витрачається на з'єднання.

`session_mode`

Цей параметр доступний починаючи з версії PHP 5 (PECL OCI8 1.1) і набуває наступних значень: **`OCI_DEFAULT`** **`OCI_SYSOPER`** і **`OCI_SYSDBA`**. Якщо були вказані \*\*`OCI_SYSOPER`** або **`OCI_SYSDBA`\*\*ця функція спробує встановити привілейоване з'єднання, використовуючи зовнішні дані авторизації. За замовчуванням привілейовані з'єднання вимкнено. Щоб їх увімкнути, необхідно встановити [oci8.privileged\_connect](oci8.configuration.md#ini.oci8.privileged-connect)в`On`

У версії PHP 5.3 (PECL OCI8 1.3.4) з'явилося значення **`OCI_CRED_EXT`**. Воно вказує Oracle використовувати зовнішню автентифікацію або автентифікацію за допомогою операційної системи, що має бути налаштовано у базі даних. Прапор **`OCI_CRED_EXT`** може бути використаний лише з ім'ям користувача "/" та порожнім паролем. . [oci8.privileged\_connect](oci8.configuration.md#ini.oci8.privileged-connect) може набувати значення `On`или`Off`

**`OCI_CRED_EXT`** може використовуватися спільно з режимами **`OCI_SYSOPER`** і **`OCI_SYSDBA`**

**`OCI_CRED_EXT`** не підтримується у Windows через безпеку.

### Значення, що повертаються

Повертає ідентифікатор з'єднання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | `connection_string` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** oci\_connect()**с синтаксисом Easy Connect**

```php
<?php

// Подключается к XE сервису (т.е. к базе данных) на "localhost"
$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT * FROM employees');
oci_execute($stid);

echo "<table border='1'>\n";
while ($row = oci_fetch_array($stid, OCI_ASSOC+OCI_RETURN_NULLS)) {
    echo "<tr>\n";
    foreach ($row as $item) {
        echo "    <td>" . ($item !== null ? htmlentities($item, ENT_QUOTES) : "") . "</td>\n";
    }
    echo "</tr>\n";
}
echo "</table>\n";

?>
```

**Приклад #2 Приклад використання** oci\_connect()**используя имя Network Connect**

```php
<?php

// Соединяется с базой данных MYDB описанной в файле tnsnames.ora,
// Приклад записи в tnsnames.ora для MYDB:
//   MYDB =
//     (DESCRIPTION =
//       (ADDRESS = (PROTOCOL = TCP)(HOST = mymachine.oracle.com)(PORT = 1521))
//       (CONNECT_DATA =
//         (SERVER = DEDICATED)
//         (SERVICE_NAME = XE)
//       )
//     )

$conn = oci_connect('hr', 'welcome', 'MYDB');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT * FROM employees');
oci_execute($stid);

echo "<table border='1'>\n";
while ($row = oci_fetch_array($stid, OCI_ASSOC+OCI_RETURN_NULLS)) {
    echo "<tr>\n";
    foreach ($row as $item) {
        echo "    <td>" . ($item !== null ? htmlentities($item, ENT_QUOTES) : "") . "</td>\n";
    }
    echo "</tr>\n";
}
echo "</table>\n";

?>
```

**Приклад #3 Приклад використання** oci\_connect()\*\* з використанням певного набору символів\*\*

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE', 'AL32UTF8');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT * FROM employees');
oci_execute($stid);

echo "<table border='1'>\n";
while ($row = oci_fetch_array($stid, OCI_ASSOC+OCI_RETURN_NULLS)) {
    echo "<tr>\n";
    foreach ($row as $item) {
        echo "    <td>" . ($item !== null ? htmlentities($item, ENT_QUOTES) : "") . "</td>\n";
    }
    echo "</tr>\n";
}
echo "</table>\n";

?>
```

**Приклад #4 Приклад використання багаторазових дзвінків **oci\_connect()****

```php
<?php

$c1 = oci_connect("hr", "welcome", 'localhost/XE');
$c2 = oci_connect("hr", "welcome", 'localhost/XE');

// $c1 и $c2 содержат одинаковый PHP id ресурса, что означает, что
// они используют одинаковое базовое соединение
echo "c1 is $c1<br>\n";
echo "c2 is $c2<br>\n";

function create_table($conn)
{
    $stmt = oci_parse($conn, "create table hallo (test varchar2(64))");
    oci_execute($stmt);
    echo "Created table<br>\n";
}

function drop_table($conn)
{
    $stmt = oci_parse($conn, "drop table hallo");
    oci_execute($stmt);
    echo "Dropped table<br>\n";
}

function insert_data($connname, $conn)
{
    $stmt = oci_parse($conn, "insert into hallo
              values(to_char(sysdate,'DD-MON-YY HH24:MI:SS'))");
    oci_execute($stmt, OCI_DEFAULT);
    echo "$connname inserted row without committing<br>\n";
}

function rollback($connname, $conn)
{
    oci_rollback($conn);
    echo "$connname rollback<br>\n";
}

function select_data($connname, $conn)
{
    $stmt = oci_parse($conn, "select * from hallo");
    oci_execute($stmt, OCI_DEFAULT);
    echo "$connname ----selecting<br>\n";
    while (oci_fetch($stmt)) {
        echo "    " . oci_result($stmt, "TEST") . "<br>\n";
    }
    echo "$connname ----done<br>\n";
}

create_table($c1);

insert_data('c1', $c1);   // Вставить строку используя c1
sleep(2);                 // остановиться для записи другой временной метки для следующей строки
insert_data('c2', $c2);   // Вставить строку используя c2

select_data('c1', $c1);   // Возврат результата обоих вставок
select_data('c2', $c2);   // Возврат результата обоих вставок

rollback('c1', $c1);      // Откат используя c1

select_data('c1', $c1);   // Откат был произведён для обоих вставок
select_data('c2', $c2);

drop_table($c1);

// Закрытие одного из соединений делает переменную PHP недоступной, но
// другие могут быть использованы
oci_close($c1);
echo "c1 is $c1<br>\n";
echo "c2 is $c2<br>\n";


// Вывод is:
//    c1 is Resource id #5
//    c2 is Resource id #5
//    Created table
//    c1 inserted row without committing
//    c2 inserted row without committing
//    c1 ----selecting
//        09-DEC-09 12:14:43
//        09-DEC-09 12:14:45
//    c1 ----done
//    c2 ----selecting
//        09-DEC-09 12:14:43
//        09-DEC-09 12:14:45
//    c2 ----done
//    c1 rollback
//    c1 ----selecting
//    c1 ----done
//    c2 ----selecting
//    c2 ----done
//    Dropped table
//    c1 is
//    c2 is Resource id #5

?>
```

### Примітки

> **Зауваження** :
> 
> Некоректно встановлений або налаштований модуль OCI8 часто повідомлятиме про проблеми з'єднання або помилки. Дивіться [Встановлення/Налаштування](oci8.setup.md)для решения проблем.

### Дивіться також

-   [oci\_pconnect()](function.oci-pconnect.md) \- Встановлює постійне з'єднання із сервером Oracle
-   [oci\_new\_connect()](function.oci-new-connect.md) \- Встановлює нове з'єднання із сервером Oracle
-   [oci\_close()](function.oci-close.md) \- Закриває з'єднання із сервером Oracle
