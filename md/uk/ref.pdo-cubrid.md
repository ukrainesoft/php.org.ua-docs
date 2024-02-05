---
navigation:
  - pdo.drivers.md: « Драйвери PDO
  - ref.pdo-cubrid.connection.md: PDO\_CUBRID DSN »
  - index.md: PHP Manual
  - pdo.drivers.md: Драйвери PDO
title: Функції CUBRID (PDO\_CUBRID)
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Функції CUBRID (PDO\_CUBRID)

## Вступ

PDO\_CUBRID - драйвер, реализующий[інтерфейс PHP Data Objects (PDO)](intro.pdo.md) доступу до баз даних CUBRID.

> **Зауваження** :
> 
> Поточна версія PDO\_CUBRID не підтримує постійні з'єднання.

## Установка

Для складання модуля PDO\_CUBRID, на тому ж хості має бути встановлений СУБД CUBRID. PDO\_CUBRID є модулем [» PECL](https://pecl.php.net/), так что для его установки следуйте инструкциям[Встановлення модулів PECL](install.pecl.md)Для указания команде**configure**директории с установленной базой CUBRID, используйте следующий синтаксис:

```
$ ./configure --with-pdo-cubrid=/path/to/CUBRID[,shared]
```

По умолчанию**configure** шукатиме відповідні бібліотеки, керуючись значенням змінної оточення CUBRID.

DLL для цього модуля PECL поки що недоступна. Дивіться також розділ [збирання на Windows](install.windows.building.md). Для більш детальної інформації про ручну установку модуля під Linux і Windows читайте build-guide.md, що міститься в пакеті PECL.

## Особливості

**Особливості PDO\_CUBRID**

| Особенности | Опис |
| --- | --- |
| Курсори, що перемотуються | PDO\_CUBRID підтримує курсори, що перемотуються. Типом курсору за промовчанням є "forward only" (тільки вперед), для його зміни можна використовувати параметр driver\_options в [PDO::prepare()](pdo.prepare.md) |
| Час очікування | PDO\_CUBRID підтримує налаштування часу очікування на виконання SQL-запиту.; Для його налаштування використовуйте метод [PDO::setAttribute()](pdo.setattribute.md) |
| Режим автопідтвердження та транзакції | PDO\_CUBRID підтримує як режим підтвердження, так і роботу з транзакціями. За промовчанням використовується режим автопідтвердження. Для зміни режиму використовуйте метод [PDO::setAttribute()](pdo.setattribute.md) |
| Якщо ви використовуєте [PDO::beginTransaction()](pdo.begintransaction.md) для старту транзакції, автопідтвердження буде автоматично заборонено і знову дозволено після [PDO::commit()](pdo.commit.md) або [PDO::rollBack()](pdo.rollback.md). . Зверніть увагу, що перед вимкненням автопідтвердження всі очікувані запити будуть автоматично підтверджені. |  |

| | Множинні SQL-запити PDO\_CUBRID підтримує численні SQL-запити. Множинні SQL-запити поділяються крапкою з комою (;) | | Інформація про схему PDO\_CUBRID реалізує функцію [PDO::cubrid\_schema()](pdo.cubrid-schema.md)для получения информации о схеме. | | LOBs | PDO\_CUBRID підтримує типи даних BLOB/CLOB. LOB PDO представляється як потік, отже ви можете вставляти LOB шляхом зв'язування з потоком і отримувати LOB шляхом читання з потоку, повернутий CUBRID PDO. Наприклад:

**Приклад #1 Вставка LOB у CUBRID PDO**

```php
<?php
$fp = fopen('lob_test.png', 'rb');

$sql_stmt = "INSERT INTO lob_test(name, content) VALUES('lob_test.png', ?)";

$stmt = $dbh->prepare($sql_stmt);
$ret = $stmt->bindParam(1, $fp, PDO::PARAM_LOB);
$ret = $stmt->execute();
?>
```

**Приклад #2 Отримання LOB у CUBRID PDO**

```php
<?php
$sql_stmt = "SELECT content FROM lob_test WHERE name='lob_test.png'";

$stmt = $dbh->prepare($sql_stmt);
$stmt->execute();
$result = $stmt->fetch(PDO::FETCH_NUM);

header("Content-Type: image/png");
fpassthru($result[0]);
?>
```

| | Метаінформація про стовпці | Метод [PDOStatement::getColumnMeta()](pdostatement.getcolumnmeta.md) в CUBRID PDO поверне асоціативний масив, що містить такі значення:

-   type
-   name
-   table
-   def
-   precision
-   scale
-   not\_null
-   auto\_increment
-   unique\_key
-   multiple\_key
-   primary\_key
-   foreign\_key
-   reverse\_index
-   reverse\_unique

| | Тип даних Колекція | PDO\_CUBRID підтримує типи даних SET/MULTISET/SEQUENCE. Якщо ви не вказуєте тип даних, то за замовчуванням буде використовуватися char. Наприклад:

**Приклад #3 Вставляє колекцію в CUBRID PDO з типом даних за замовчуванням.**

```php
<?php
$conn_str ="cubrid:dbname=demodb;host=localhost;port=33000";
$cubrid_pdo = new PDO($conn_str, 'dba', '');

$cubrid_pdo->exec("DROP TABLE if exists test_tbl");
$cubrid_pdo->exec("CREATE TABLE test_tbl (col_1 SET(VARCHAR))");

$sql_stmt_insert = "INSERT INTO test_tbl VALUES (?);";
$stmt = $cubrid_pdo->prepare($sql_stmt_insert);
$data = array("abc","def","ghi");
$ret = $stmt->bindParam(1, $data, PDO::PARAM_NULL);
$ret = $stmt->execute();
var_Dump($ret);
?>
```

**Приклад #4 Вказує тип даних при вставці колекції в CUBRID PDO**

```php
<?php
$conn_str ="cubrid:dbname=demodb;host=localhost;port=33000";
$cubrid_pdo = new PDO($conn_str, 'dba', '');

$cubrid_pdo->exec("DROP TABLE if exists test_tbl");
$cubrid_pdo->exec("CREATE TABLE test_tbl (col_1 SET(int))");

$sql_stmt_insert = "INSERT INTO test_tbl VALUES (?);";
$stmt = $cubrid_pdo->prepare($sql_stmt_insert);
$data = array(1,2,3,4);
$ret = $stmt->bindParam(1, $data, 0,0,"int");
$ret = $stmt->execute();
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

Наведені нижче константи визначені цим драйвером і будуть доступні лише у випадку, якщо PHP був зібраний за допомогою цього модуля, або модуль був динамічно завантажений під час виконання. Крім того, ці залежні від драйвера константи повинні бути використані лише разом із цим драйвером. Використання атрибутів, специфічних для деякого драйвера з іншим драйвером, може викликати несподівану поведінку. Якщо ваш код виконується з кількома драйверами, можна використовувати функцію [PDO::getAttribute()](pdo.getattribute.md)для получения атрибута\*\*`PDO::ATTR_DRIVER_NAME`\*\*для проверки драйвера.

Наведені нижче константи можна використовувати для встановлення атрибутів бази даних. Ці константи можна використовувати з функціями [PDO::getAttribute()](pdo.getattribute.md) і [PDO::setAttribute()](pdo.setattribute.md)

**Прапори атрибутів PDO::CUBRID**

| Константы | Опис |
| --- | --- |
| PDO::CUBRID\_ATTR\_ISOLATION\_LEVEL | Рівень ізоляції для з'єднання. |
| PDO::CUBRID\_ATTR\_LOCK\_TIMEOUT | Час очікування транзакції за секунди. |
| PDO::CUBRID\_ATTR\_MAX\_STRING\_LENGTH | Лише для читання. Максимальна довжина рядка для типів даних bit, varbit, char, varchar, nchar, nchar під час використання CUBRID PDO API. |

Наступні константи можна використовувати для встановлення рівня ізоляції транзакції. Ці константи можна використовувати з функціями [PDO::getAttribute()](pdo.getattribute.md) і [PDO::setAttribute()](pdo.setattribute.md)

**Прапори рівнів ізоляції PDO::CUBRID**

| Константы | Опис |
| --- | --- |
| PDO::TRAN\_COMMIT\_CLASS\_UNCOMMIT\_INSTANCE | Найнижчий рівень ізоляції (1). Можливе брудне, неповторне або фантомне читання для кортежів та неповторне читання для таблиці. |
| PDO::TRAN\_COMMIT\_CLASS\_COMMIT\_INSTANCE | Відносно низький рівень ізоляції (2). Брудного читання не буде, але неповторне або фантомне можливо. |
| PDO::TRAN\_REP\_CLASS\_UNCOMMIT\_INSTANCE | Рівень ізоляції CUBRID за промовчанням (3). Можливо брудне, неповторне або фантомне читання для кортежів, але для таблиць гарантовано читання, що повторюється. |
| PDO::TRAN\_REP\_CLASS\_COMMIT\_INSTANCE | Відносно низький рівень ізоляції (4). Брудного читання не буде, але неповторне або фантомне можливо. |
| PDO::TRAN\_REP\_CLASS\_REP\_INSTANCE | Відносно високий рівень ізоляції (5). Брудного та неповторного читання не буде, але фантомне може виникнути. |
| PDO::TRAN\_SERIALIZABLE | Найвищий рівень ізоляції (6). Брудне, неповторне та фантомне читання неможливі. |

Наступні константи використовуються для отримання інформації схеми. Можуть використовуватись із функцією [PDO::cubrid\_schema()](pdo.cubrid-schema.md)

**Прапори схеми PDO::CUBRID**

| Константы | Опис |
| --- | --- |
| PDO::CUBRID\_SCH\_TABLE | Отримання імені та типу таблиці CUBRID. |
| PDO::CUBRID\_SCH\_VIEW | Отримання імені та типу view у CUBRID. |
| PDO::CUBRID\_SCH\_QUERY\_SPEC | Отримання SQL-запиту, з допомогою якого створено view. |
| PDO::CUBRID\_SCH\_ATTRIBUTE | Отримання атрибутів стовпця таблиці. |
| PDO::CUBRID\_SCH\_TABLE\_ATTRIBUTE | Одержання атрибутів таблиці. |
| PDO::CUBRID\_SCH\_METHOD | Отримання методу екземпляра. Метод екземпляра – це метод викликаний екземпляром класу. Використовується значно частіше, ніж метод класу, оскільки більшість операцій провадиться в екземплярі. |
| PDO::CUBRID\_SCH\_TABLE\_METHOD | Отримати метод класу. Метод класу - це метод викликаний об'єктом класу. Зазвичай використовується до створення нового екземпляра класу чи його ініціалізації. Також використовується для доступу та зміни атрибутів класу. |
| PDO::CUBRID\_SCH\_METHOD\_FILE | Отримати інформацію про файл, де визначено метод таблиці. |
| PDO::CUBRID\_SCH\_SUPER\_TABLE | Отримати ім'я та тип таблиці, чиї атрибути успадковуються зазначеною таблицею. |
| PDO::CUBRID\_SCH\_SUB\_TABLE | Отримати ім'я та тип таблиці, яка успадковує вказані атрибути. |
| PDO::CUBRID\_SCH\_CONSTRAINT | Отримати обмеження таблиці. |
| PDO::CUBRID\_SCH\_TRIGGER | Отримати тригер таблиці. |
| PDO::CUBRID\_SCH\_TABLE\_PRIVILEGE | Отримати інформацію про права таблиці. |
| PDO::CUBRID\_SCH\_COL\_PRIVILEGE | Отримати інформацію про права на стовпець. |
| PDO::CUBRID\_SCH\_DIRECT\_SUPER\_TABLE | Отримати пряму супер таблицю для заданої таблиці. |
| PDO::CUBRID\_SCH\_PRIMARY\_KEY | Отримати первинний ключ таблиці. |
| PDO::CUBRID\_SCH\_IMPORTED\_KEYS | Отримати імпортовані ключі для таблиці. |
| PDO::CUBRID\_SCH\_EXPORTED\_KEYS | Отримати експортовані ключі для таблиці. |
| PDO::CUBRID\_SCH\_CROSS\_REFERENCE | Отримати зв'язки двох таблиць. |

## Зміст

-   [PDO\_CUBRID DSN](ref.pdo-cubrid.connection.md)— З'єднання з базою даних CUBRID
-   [PDO::cubrid\_schema](pdo.cubrid-schema.md)— Отримати запитану інформацію про схему
