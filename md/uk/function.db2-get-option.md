---
navigation:
  - function.db2-free-stmt.md: « db2freestmt
  - function.db2-last-insert-id.md: db2lastinsertid »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2getoption
---
# db2getoption

(PECL ibmdb2> = 1.6.0)

db2getoption — Встановлює параметр для ресурсу оператора або ресурсу з'єднання.

### Опис

```methodsynopsis
db2_get_option(resource $resource, string $option): string|false
```

Виймає значення вказаного параметра для ресурсу оператора або з'єднання.

### Список параметрів

`resource`

Допустимий ресурс оператора, що повертається [db2prepare()](function.db2-prepare.md) або допустимий ресурс з'єднання, що повертається [db2connect()](function.db2-connect.md) або [db2pconnect()](function.db2-pconnect.md)

`option`

Допустимий оператор або варіанти підключення. Наступні нові параметри доступні в ibmDB2 версії 1.6.0. Вони надають корисну інформацію для відстеження, яку можна встановити під час виконання за допомогою **db2getoption()**

> **Зауваження**
> 
> Попередні версії ibmdb2 не підтримують нові параметри.
> 
> Коли встановлюється значення кожної опції, деякі сервери можуть обробляти всю надану довжину і можуть усікати значення.
> 
> Щоб забезпечити правильне перетворення даних, зазначених у кожній опції, під час передачі в хост-систему, використовуйте лише символи від A до Z, від 0 до 9, знак підкреслення () або точку (.).

`userid`

`SQL_ATTR_INFO_USERID` - Вказівник на символьний рядок із завершальним нулем, що використовується для ідентифікації ID користувача клієнта, що надсилається на сервер бази даних хоста під час використання DB2 Connect.

> **Зауваження**
> 
> Сервери DB2 для z/OS та OS/390 підтримують довжину до 16 символів. Ідентифікатор користувача не слід плутати з ідентифікатором користувача для автентифікації, він використовується тільки для цілей ідентифікації і не використовується для авторизації.

`acctstr`

`SQL_ATTR_INFO_ACCTSTR` - Вказівник на символьний рядок із завершальним нулем, що використовується для ідентифікації облікового рядка клієнта, що надсилається на сервер бази даних хоста під час використання DB2 Connect.

> **Зауваження**
> 
> Сервери DB2 для z/OS та OS/390 підтримують довжину до 200 символів.

`applname`

`SQL_ATTR_INFO_APPLNAME` - Вказівник на символьний рядок із завершальним нулем, що використовується для ідентифікації імені клієнтської програми, що надсилається на сервер бази даних хоста під час використання DB2 Connect.

> **Зауваження**
> 
> Сервери DB2 для z/OS та OS/390 підтримують довжину до 32 символів.

`wrkstnname`

`SQL_ATTR_INFO_WRKSTNNAME` - Вказівник на символьний рядок із завершальним нулем, що використовується для ідентифікації імені клієнтської програми, що надсилається на сервер бази даних хоста під час використання DB2 Connect.

> **Зауваження**
> 
> Сервери DB2 для z/OS та OS/390 підтримують довжину до 18 символів.

У наступній таблиці наведено параметри, сумісні з доступними типами ресурсів:

**Матриця параметрів ресурсів**

| Ключ | Значение | Тип ресурса |
| --- | --- | --- |
|  |  | Connection |
| userid | `SQL_ATTR_INFO_USERID` | З |
| acctstr | `SQL_ATTR_INFO_ACCTSTR` | З |
| applname | `SQL_ATTR_INFO_APPLNAME` | З |
| wrkstnname | `SQL_ATTR_INFO_WRKSTNNAME` | З |

### Значення, що повертаються

Повертає поточне налаштування атрибута підключення, надане у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Встановлення та отримання параметрів через ресурс підключення**

```php
<?php
/* Параметры подключения к базе данных */
$database = 'SAMPLE';
$user     = 'db2inst1';
$password = 'ibmdb2';

/* Получение ресурса подключения */
$conn = db2_connect($database, $user, $password);

echo "Атрибуты клиента, передаваемые через строку подключения:\n";

/* Создайте Масив ассоциативных опций с допустимыми парами "ключ-значение" */
/* Назначьте атрибуты через строку подключения */
/* Доступ к указанным параметрам */
$options1 = array('userid' => 'db2inst1');
$conn1 = db2_connect($database, $user, $password, $options1);
$val = db2_get_option($conn1, 'userid');
echo $val . "\n";

$options2 = array('acctstr' => 'account');
$conn2 = db2_connect($database, $user, $password, $options2);
$val = db2_get_option($conn2, 'acctstr');
echo $val . "\n";

$options3 = array('applname' => 'myapp');
$conn3 = db2_connect($database, $user, $password, $options3);
$val = db2_get_option($conn3, 'applname');
echo $val . "\n";

$options4 = array('wrkstnname' => 'workstation');
$conn4 = db2_connect($database, $user, $password, $options4);
$val = db2_get_option($conn4, 'wrkstnname');
echo $val . "\n";

echo "Атрибуты клиента прошли после подключения:\n";

/* Create the associative options array with valid key-value pairs */
/* Assign the attributes after a connection is made */
/* Access the options specified */
$options5 = array('userid' => 'db2inst1');
$conn5 = db2_connect($database, $user, $password);
$rc = db2_set_option($conn5, $options5, 1);
$val = db2_get_option($conn5, 'userid');
echo $val . "\n";

$options6 = array('acctstr' => 'account');
$conn6 = db2_connect($database, $user, $password);
$rc = db2_set_option($conn6, $options6, 1);
$val = db2_get_option($conn6, 'acctstr');
echo $val . "\n";

$options7 = array('applname' => 'myapp');
$conn7 = db2_connect($database, $user, $password);
$rc = db2_set_option($conn7, $options7, 1);
$val = db2_get_option($conn7, 'applname');
echo $val . "\n";

$options8 = array('wrkstnname' => 'workstation');
$conn8 = db2_connect($database, $user, $password);
$rc = db2_set_option($conn8, $options8, 1);
$val = db2_get_option($conn8, 'wrkstnname');
echo $val . "\n";
?>
```

Результат виконання цього прикладу:

```
Атрибуты клиента, передаваемые через строку подключения
db2inst1
account
myapp
workstation
Атрибуты клиента прошли после подключения:
db2inst1
account
myapp
workstation
```

### Дивіться також

-   [db2connect()](function.db2-connect.md) - Повертає з'єднання з базою даних
-   [db2cursortype()](function.db2-cursor-type.md) - Повертає тип курсору, який використовується у ресурсі оператора
-   [db2exec()](function.db2-exec.md) - Виконує SQL-запит безпосередньо
-   [db2setoption()](function.db2-set-option.md) - Встановлення опції для з'єднання або ресурсу оператора
-   [db2pconnect()](function.db2-pconnect.md) - Повертає постійне з'єднання з базою даних
-   [db2prepare()](function.db2-prepare.md) - готує SQL-запит до виконання
