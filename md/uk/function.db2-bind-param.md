---
navigation:
  - function.db2-autocommit.md: « db2autocommit
  - function.db2-client-info.md: db2clientinfo »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2bindparam
---
# db2bindparam

(PECL ibmdb2> = 1.0.0)

db2bindparam — Зв'язує змінну PHP із параметром SQL-виразу

### Опис

```methodsynopsis
db2_bind_param(    resource $stmt,    int $parameter_number,    string $variable_name,    int $parameter_type = ?,    int $data_type = 0,    int $precision = -1,    int $scale = 0): bool
```

Зв'язує змінну PHP з параметром SQL-вираження у виразному ресурсі, що повертається [db2prepare()](function.db2-prepare.md). Ця функція дає більший контроль над типом параметра, типом даних, точністю та масштабом для параметра, ніж проста передача змінної як частини необов'язкового вхідного масиву [db2execute()](function.db2-execute.md)

### Список параметрів

`stmt`

Підготовлений вираз, що повертається [db2prepare()](function.db2-prepare.md)

`parameter_number`

Задає позицію параметра, що нумерується з 1 у підготовленому виразі.

`variable_name`

Рядок, що визначає ім'я змінної PHP для прив'язки до параметра, заданого `parameter_number`

`parameter_type`

Константа, що визначає, чи має змінна PHP бути прив'язана до параметра SQL як вхідний параметр (`DB2_PARAM_IN`), вихідний параметр (`DB2_PARAM_OUT`) або або як параметр, що приймає введення та повертає висновок (`DB2_PARAM_INOUT`). Щоб уникнути перевантаження пам'яті, можна також вказати `DB2_PARAM_FILE`, щоб прив'язати змінну PHP до імені файлу, який містить дані великого об'єкта (BLOB, CLOB або DBCLOB).

`data_type`

Константа, що вказує тип даних SQL, з яким має бути пов'язана змінна PHP: `DB2_BINARY` `DB2_CHAR` `DB2_DOUBLE` або `DB2_LONG`

`precision`

Задає точність, з якою змінна має бути прив'язана до бази даних. Цей параметр також можна використовувати для отримання вихідних значень XML зі збережених процедур. Невід'ємне значення вказує максимальний розмір даних XML, які будуть вилучені з бази даних. Якщо цей параметр не використовується, для отримання вихідного значення XML із процедури, що зберігається, передбачається значення за замовчуванням 1 МБ.

`scale`

Задає масштаб, з яким змінна має бути прив'язана до бази даних.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Прив'язка змінних PHP до підготовленого виразу**

SQL-вираз у цьому прикладі використовує два вхідні параметри в пропозиції WHERE. Викликається **db2bindparam()**, щоб зв'язати дві змінні PHP із відповідними параметрами SQL. Зверніть увагу, що змінні PHP не потрібно оголошувати або надавати перед викликом **db2bindparam()**; у цьому прикладі `$lower_limit` надається значення перед викликом **db2bindparam()**, а `$upper_limit` надається значення після виклику **db2bindparam()**. Перед викликом [db2execute()](function.db2-execute.md) змінні мають бути пов'язані, а параметрам, що приймають введення, має бути присвоєно будь-яке значення . [db2execute()](function.db2-execute.md)

```php
<?php

$sql = 'SELECT name, breed, weight FROM animals
    WHERE weight > ? AND weight < ?';
$conn = db2_connect($database, $user, $password);
$stmt = db2_prepare($conn, $sql);

// Можно объявить переменную перед вызовом db2_bind_param()
$lower_limit = 1;

db2_bind_param($stmt, 1, "lower_limit", DB2_PARAM_IN);
db2_bind_param($stmt, 2, "upper_limit", DB2_PARAM_IN);

// Также можно объявить переменную после вызова db2_bind_param()
$upper_limit = 15.0;

if (db2_execute($stmt)) {
    while ($row = db2_fetch_array($stmt)) {
        print "{$row[0]}, {$row[1]}, {$row[2]}\n";
    }
}
?>
```

Результат виконання цього прикладу:

```
Pook, cat, 3.2
Rickety Ride, goat, 9.7
Peaches, dog, 12.3
```

**Приклад #2 Виклик збережених процедур з параметрами IN та OUT**

Зберігається процедура matchanimal в даному прикладі приймає три різні параметри:

1.  вхідний параметр (IN), який приймає ім'я першої тварини як вхідні дані
    
2.  параметр вводу-виводу (INOUT), який приймає ім'я другої тварини як вхідні дані та повертає рядок `TRUE`якщо тварина в базі даних збігається з цим ім'ям
    
3.  вихідний параметр (OUT), який повертає суму ваги двох ідентифікованих тварин
    

Крім того, процедура, що зберігається, повертає набір результатів, що складається з тварин, перерахованих в алфавітному порядку, починаючи з тварини, що відповідає вхідному значенню першого параметра, і закінчуючи тваринам, відповідним вхідному значенню другого параметра.

```php
<?php

$sql = 'CALL match_animal(?, ?, ?)';
$conn = db2_connect($database, $user, $password);
$stmt = db2_prepare($conn, $sql);

$name = "Peaches";
$second_name = "Rickety Ride";
$weight = 0;

db2_bind_param($stmt, 1, "name", DB2_PARAM_IN);
db2_bind_param($stmt, 2, "second_name", DB2_PARAM_INOUT);
db2_bind_param($stmt, 3, "weight", DB2_PARAM_OUT);

print "Values of bound parameters _before_ CALL:\n";
print "  1: {$name} 2: {$second_name} 3: {$weight}\n\n";

if (db2_execute($stmt)) {
    print "Values of bound parameters _after_ CALL:\n";
    print "  1: {$name} 2: {$second_name} 3: {$weight}\n\n";

    print "Results:\n";
    while ($row = db2_fetch_array($stmt)) {
        print "  {$row[0]}, {$row[1]}, {$row[2]}\n";
    }
}
?>
```

Результат виконання цього прикладу:

```
Values of bound parameters _before_ CALL:
  1: Peaches 2: Rickety Ride 3: 0

Values of bound parameters _after_ CALL:
  1: Peaches 2: TRUE 3: 22

Results:
  Peaches, dog, 12.3
  Pook, cat, 3.2
  Rickety Ride, goat, 9.7
```

**Приклад #3 Вставлення великого двійкового об'єкта (BLOB) безпосередньо з файлу**

Дані великих об'єктів зазвичай зберігаються у файлах, таких як документи XML або аудіофайли. Замість того, щоб зчитувати весь файл у змінну PHP і потім пов'язувати цю змінну PHP з SQL-виразом, можна уникнути деяких накладних витрат на пам'ять, прив'язавши файл безпосередньо до вхідного параметра SQL-виразу. У цьому прикладі показано, як безпосередньо прив'язати файл до стовпця BLOB.

```php
<?php
$stmt = db2_prepare($conn, "INSERT INTO animal_pictures(picture) VALUES (?)");

$picture = "/opt/albums/spook/grooming.jpg";
$rc = db2_bind_param($stmt, 1, "picture", DB2_PARAM_FILE);
$rc = db2_execute($stmt);
?>
```

### Дивіться також

-   [db2execute()](function.db2-execute.md) - Виконує підготовлений SQL-запит
-   [db2prepare()](function.db2-prepare.md) - готує SQL-запит до виконання
