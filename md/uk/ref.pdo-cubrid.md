Функції CUBRID (PDOCUBRID)

-   [« Драйверы PDO](pdo.drivers.html)
    
-   [PDO\_CUBRID DSN »](ref.pdo-cubrid.connection.html)
    
-   [PHP Manual](index.html)
    
-   [Драйверы PDO](pdo.drivers.html)
    
-   Функції CUBRID (PDOCUBRID)
    

# Функції CUBRID (PDOCUBRID)

## Вступ

PDOCUBRID – драйвер, що реалізує [интерфейс PHP Data Objects (PDO)](intro.pdo.html) доступу до баз даних CUBRID.

> **Зауваження**
> 
> Поточна версія PDOCUBRID не підтримує постійні з'єднання.

## Встановлення

Для складання модуля PDOCUBRID, на тому ж хості має бути встановлений СУБД CUBRID. PDOCUBRID є модулем [» PECL](https://pecl.php.net/), так що для його встановлення дотримуйтесь інструкцій [Установка модулей PECL](install.pecl.html). Для вказівки команді **configure** директорії із встановленою базою CUBRID, використовуйте наступний синтаксис:

```
$ ./configure --with-pdo-cubrid=/path/to/CUBRID[,shared]
```

За замовчуванням **configure** шукатиме відповідні бібліотеки, керуючись значенням змінної оточення `CUBRID`

DLL для цього модуля PECL зараз недоступна. Дивіться також розділ [сборка на Windows](install.windows.building.html). Для більш детальної інформації про ручну установку модуля під Linux і Windows читайте build-guide.html, що міститься в пакеті PECL.

## Відмітні особливості

**Відмінні риси PDOCUBRID**

| Отличительные особенности                                                                                                                                                                                                                                                                                                                                           | Описание                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Курсори, що перемотуються                                                                                                                                                                                                                                                                                                                                           | PDOCUBRID підтримує курсори, що перемотуються. Типом курсору за промовчанням є "forward only" (тільки вперед), для його зміни можна використовувати параметр driveroptions в [PDO::prepare()](pdo.prepare.html)       |
| Час очікування                                                                                                                                                                                                                                                                                                                                                      | PDOCUBRID підтримує налаштування часу очікування на виконання SQL-запиту.; Для його налаштування використовуйте метод [PDO::setAttribute()](pdo.setattribute.html)                                                    |
| Режим автопідтвердження та транзакції                                                                                                                                                                                                                                                                                                                               | PDOCUBRID підтримує як режим підтвердження, так і роботу з транзакціями. За промовчанням використовується режим автопідтвердження. Для зміни режиму використовуйте метод [PDO::setAttribute()](pdo.setattribute.html) |
| Якщо ви використовуєте [PDO::beginTransaction()](pdo.begintransaction.html) для старту транзакції, автопідтвердження буде автоматично заборонено і знову дозволено після [PDO::commit()](pdo.commit.html) або [PDO::rollBack()](pdo.rollback.html). Зверніть увагу, що перед вимкненням автопідтвердження всі запити, що очікують, будуть автоматично підтверджені. |                                                                                                                                                                                                                       |

| | Множинні SQL-запити PDOCUBRID підтримує численні SQL-запити. Множинні SQL-запити поділяються крапкою з комою (;) | | Інформація про схему PDOCUBRID реалізує функцію [PDO::cubrid\_schema()](pdo.cubrid-schema.html) для отримання інформації про схему. | | LOBs | PDOCUBRID підтримує типи даних BLOB/CLOB. LOB PDO представляється як потік, отже ви можете вставляти LOB шляхом зв'язування з потоком і отримувати LOB шляхом читання з потоку, повернутий CUBRID PDO. Наприклад:

**Приклад #1 Вставка LOB у CUBRID PDO**

```php
<?php
$fp = fopen('lob_test.png', 'rb');

$sql_stmt = "INSERT INTO lob_test(name, content) VALUES('lob_test.png', ?)";

$stmt = $dbh->prepare($sql_stmt);
$ret = $stmt->bindParam(1, $fp, PDO::PARAM_LOB);
$ret = $stmt->execute();
?>
```

**Приклад #2 Отримання LOB у CUBRID PDO**

```php
<?php
$sql_stmt = "SELECT content FROM lob_test WHERE name='lob_test.png'";

$stmt = $dbh->prepare($sql_stmt);
$stmt->execute();
$result = $stmt->fetch(PDO::FETCH_NUM);

header("Content-Type: image/png");
fpassthru($result[0]);
?>
```

| | Метаінформація про стовпці | Метод [PDOStatement::getColumnMeta()](pdostatement.getcolumnmeta.html) в CUBRID PDO поверне асоціативний масив, що містить такі значення:

-   type
-   name
-   table
-   def
-   precision
-   scale
-   notnull
-   autoincrement
-   uniquekey
-   multiplekey
-   primarykey
-   foreignkey
-   reverseindex
-   reverseunique

| | Тип даних Колекція | PDOCUBRID підтримує типи даних SET/MULTISET/SEQUENCE. Якщо ви не вказуєте тип даних, то за замовчуванням буде використовуватися char. Наприклад:

**Приклад #3 Вставляє колекцію в CUBRID PDO з типом даних за замовчуванням.**

```php
<?php
$conn_str ="cubrid:dbname=demodb;host=localhost;port=33000";
$cubrid_pdo = new PDO($conn_str, 'dba', '');

$cubrid_pdo->exec("DROP TABLE if exists test_tbl");
$cubrid_pdo->exec("CREATE TABLE test_tbl (col_1 SET(VARCHAR))");

$sql_stmt_insert = "INSERT INTO test_tbl VALUES (?);";
$stmt = $cubrid_pdo->prepare($sql_stmt_insert);
$data = array("abc","def","ghi");
$ret = $stmt->bindParam(1, $data, PDO::PARAM_NULL);
$ret = $stmt->execute();
var_Dump($ret);
?>
```

**Приклад #4 Вказує тип даних при вставці колекції в CUBRID PDO**

```php
<?php
$conn_str ="cubrid:dbname=demodb;host=localhost;port=33000";
$cubrid_pdo = new PDO($conn_str, 'dba', '');

$cubrid_pdo->exec("DROP TABLE if exists test_tbl");
$cubrid_pdo->exec("CREATE TABLE test_tbl (col_1 SET(int))");

$sql_stmt_insert = "INSERT INTO test_tbl VALUES (?);";
$stmt = $cubrid_pdo->prepare($sql_stmt_insert);
$data = array(1,2,3,4);
$ret = $stmt->bindParam(1, $data, 0,0,"int");
$ret = $stmt->execute();
var_Dump($ret);
?>
```

Типи даних CUBRID:(п'ятий параметр PDOStatement::bindParam):

-   CHAR
-   STRING
-   NCHAR
-   VARNCHAR
-   BIT
-   VARBIT
-   NUMERIC
-   NUMBER
-   INT
-   SHORT
-   BIGINT
-   MONETARY
-   FLOAT
-   DOUBLE
-   DATE
-   TIME
-   DATETIME
-   TIMESTAMP

## Обумовлені константи

Наведені нижче константи визначені цим драйвером і будуть доступні лише у випадку, якщо PHP був зібраний з підтримкою цього модуля, або цей модуль був динамічно завантажений під час виконання. Крім того, ці залежні від драйвера константи повинні бути використані лише разом із цим драйвером. Використання атрибутів, специфічних для деякого драйвера з іншим драйвером, може викликати несподівану поведінку. Якщо ваш код виконується з кількома драйверами, можна використовувати функцію [PDO::getAttribute()](pdo.getattribute.html) для отримання атрибуту **`PDO::ATTR_DRIVER_NAME`** для перевірки драйвера.

Наведені нижче константи можна використовувати для встановлення атрибутів бази даних. Ці константи можна використовувати з функціями [PDO::getAttribute()](pdo.getattribute.html) і [PDO::setAttribute()](pdo.setattribute.html)

**Прапори атрибутів PDO::CUBRID**

| Константы                      | Описание                                                                                                                                  |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| PDO::CUBRIDATTRISOLATIONLEVEL  | Рівень ізоляції для з'єднання.                                                                                                            |
| PDO::CUBRIDATTRLOCKTIMEOUT     | Час очікування транзакції за секунди.                                                                                                     |
| PDO::CUBRIDATTRMAXSTRINGLENGTH | Лише для читання. Максимальна довжина рядка для типів даних bit, varbit, char, varchar, nchar, nchar під час використання CUBRID PDO API. |

Наступні константи можна використовувати для встановлення рівня ізоляції транзакції. Ці константи можна використовувати з функціями [PDO::getAttribute()](pdo.getattribute.html) і [PDO::setAttribute()](pdo.setattribute.html)

**Прапори рівнів ізоляції PDO::CUBRID**

| Константы                            | Описание                                                                                                                                                        |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PDO::TRANCOMMITCLASSUNCOMMITINSTANCE | Найнижчий рівень ізоляції (1). Можливе брудне, неповторне або фантомне читання для кортежів та неповторне читання для таблиці.                                  |
| PDO::TRANCOMMITCLASSCOMMITINSTANCE   | Відносно низький рівень ізоляції (2). Брудного читання не буде, але неповторне або фантомне можливо.                                                            |
| PDO::TRANREPCLASSUNCOMMITINSTANCE    | Рівень ізоляції CUBRID за промовчанням (3). Можливо брудне, неповторне або фантомне читання для кортежів, але для таблиць гарантовано читання, що повторюється. |
| PDO::TRANREPCLASSCOMMITINSTANCE      | Відносно низький рівень ізоляції (4). Брудного читання не буде, але неповторне або фантомне можливо.                                                            |
| PDO::TRANREPCLASSREPINSTANCE         | Відносно високий рівень ізоляції (5). Брудного та неповторного читання не буде, але фантомне може виникнути.                                                    |
| PDO::TRANSERIALIZABLE                | Найвищий рівень ізоляції (6). Брудне, неповторне та фантомне читання неможливі.                                                                                 |

Наступні константи використовуються для отримання інформації схеми. Можуть використовуватись із функцією [PDO::cubrid\_schema()](pdo.cubrid-schema.html)

**Прапори схеми PDO::CUBRID**

| Константы                      | Описание                                                                                                                                                                                                                   |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PDO::CUBRIDSCHTABLE            | Отримання імені та типу таблиці CUBRID.                                                                                                                                                                                    |
| PDO::CUBRIDSCHVIEW             | Отримання імені та типу view у CUBRID.                                                                                                                                                                                     |
| PDO::CUBRIDSCHQUERYSPEC        | Отримання SQL-запиту, з допомогою якого створено view.                                                                                                                                                                     |
| PDO::CUBRIDSCHATTRIBUTE        | Отримання атрибутів стовпця таблиці.                                                                                                                                                                                       |
| PDO::CUBRIDSCHTABLEATTRIBUTE   | Одержання атрибутів таблиці.                                                                                                                                                                                               |
| PDO::CUBRIDSCHMETHOD           | Отримання методу екземпляра. Метод екземпляра – це метод викликаний екземпляром класу. Використовується значно частіше, ніж метод класу, оскільки більшість операцій провадиться в екземплярі.                             |
| PDO::CUBRIDSCHTABLEMETHOD      | Отримати метод класу. Метод класу - це метод викликаний об'єктом класу. Зазвичай використовується до створення нового екземпляра класу чи його ініціалізації. Також використовується для доступу та зміни атрибутів класу. |
| PDO::CUBRIDSCHMETHODFILE       | Отримати інформацію про файл, де визначено метод таблиці.                                                                                                                                                                  |
| PDO::CUBRIDSCHSUPERTABLE       | Отримати ім'я та тип таблиці, чиї атрибути успадковуються вказаною таблицею.                                                                                                                                               |
| PDO::CUBRIDSCHSUBTABLE         | Отримати ім'я та тип таблиці, яка успадковує вказані атрибути.                                                                                                                                                             |
| PDO::CUBRIDSCHCONSTRAINT       | Отримати обмеження таблиці.                                                                                                                                                                                                |
| PDO::CUBRIDSCHTRIGGER          | Отримати тригер таблиці.                                                                                                                                                                                                   |
| PDO::CUBRIDSCHTABLEPRIVILEGE   | Отримати інформацію про права таблиці.                                                                                                                                                                                     |
| PDO::CUBRIDSCHCOLPRIVILEGE     | Отримати інформацію про права на стовпець.                                                                                                                                                                                 |
| PDO::CUBRIDSCHDIRECTSUPERTABLE | Отримати пряму супер таблицю для заданої таблиці.                                                                                                                                                                          |
| PDO::CUBRIDSCHPRIMARYKEY       | Отримати первинний ключ таблиці.                                                                                                                                                                                           |
| PDO::CUBRIDSCHIMPORTEDKEYS     | Отримати імпортовані ключі для таблиці.                                                                                                                                                                                    |
| PDO::CUBRIDSCHEXPORTEDKEYS     | Отримати експортовані ключі для таблиці.                                                                                                                                                                                   |
| PDO::CUBRIDSCHCROSSREFERENCE   | Отримати зв'язки двох таблиць.                                                                                                                                                                                             |

## Зміст

-   [PDO\_CUBRID DSN](ref.pdo-cubrid.connection.html) — З'єднання з базою даних CUBRID
-   [PDO::cubrid\_schema](pdo.cubrid-schema.html) — Отримати запитану інформацію про схему