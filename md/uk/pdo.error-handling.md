---
navigation:
  - pdo.prepared-statements.md: '« Підготовлені запити та процедури, що зберігаються'
  - pdo.lobs.md: Великі об'єкти (LOB) »
  - index.md: PHP Manual
  - book.pdo.md: PDO
title: Помилки та їх обробка
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Помилки та їх обробка

PDO пропонує вибір 3 стратегії обробки помилок в залежності від вашого стилю розробки додатків.

-   **`PDO::ERRMODE_SILENT`**
    
    До PHP 8.0.0 це був режим за замовчуванням. PDO просто надасть вам код помилки, який можна отримати методами[PDO::errorCode()](pdo.errorcode.md) і [PDO::errorInfo()](pdo.errorinfo.md). Ці методи реалізовані як і об'єктах запитів, і у об'єктах баз даних. Якщо помилка викликана під час виконання коду об'єкта запиту, потрібно викликати метод[PDOStatement::errorCode()](pdostatement.errorcode.md) або [PDOStatement::errorInfo()](pdostatement.errorinfo.md)цього об'єкта. Якщо помилка виклику об'єкта бази даних, потрібно викликати аналогічні методи цього об'єкта.
    
-   **`PDO::ERRMODE_WARNING`**
    
    Крім встановлення коду помилки PDO видасть звичайне E\_WARNING повідомлення. Це може бути корисним при налагодженні або тестуванні, коли потрібно бачити, що сталося, але не потрібно переривати роботу програми.
    
-   **`PDO::ERRMODE_EXCEPTION`**
    
    Починаючи з PHP 8.0.0 є стандартним режимом. Крім завдання коду помилки PDO викидатиме виняток[PDOException](class.pdoexception.md), властивості якого відображатимуть код помилки та її опис. Цей режим також корисний при налагодженні, тому що відразу відомо, де в програмі сталася помилка. Це дозволяє швидко локалізувати та вирішити проблему. (Не забувайте, що якщо виняток є причиною завершення роботи скрипту, всі активні транзакції будуть відкачені.)
    
    Режим винятків також корисний, тому що дає можливість структурувати обробку помилок більш ретельно, ніж зі звичайними попередженнями PHP, а також з меншою вкладеністю коду, ніж у випадку роботи в тихому режимі з явною перевіркою значень, що повертаються при кожному зверненні до бази даних.
    
    Докладніше про винятки в PHP дивіться у розділі[Винятки](language.exceptions.md)
    

PDO стандартизовано для роботи з рядковими кодами помилок SQL-92 SQLSTATE. Окремі драйвери PDO можуть задавати відповідність власних кодів кодам SQLSTATE. Метод [PDO::errorCode()](pdo.errorcode.md) повертає одиночний код SQLSTATE. Якщо потрібна специфічна інформація про помилку, PDO пропонує метод [PDO::errorInfo()](pdo.errorinfo.md), який повертає масив, що містить код SQLSTATE, код помилки драйвера, а також рядок помилки драйвера.

**Приклад #1 Створення PDO об'єкта та встановлення режиму обробки помилок**

```php
<?php
$dsn = 'mysql:dbname=testdb;host=127.0.0.1';
$user = 'dbuser';
$password = 'dbpass';

$dbh = new PDO($dsn, $user, $password);
$dbh->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);

// PDO выбросит исключение PDOException (если таблица не существует)
$dbh->query("SELECT wrongcolumn FROM wrongtable");
?>
```

Результат виконання наведеного прикладу:

```
Fatal error: Uncaught PDOException: SQLSTATE[42S02]: Base table or view not found: 1146 Table 'testdb.wrongtable' doesn't exist in /tmp/pdo_test.php:10
Stack trace:
#0 /tmp/pdo_test.php(10): PDO->query('SELECT wrongcol...')
#1 {main}
  thrown in /tmp/pdo_test.php on line 10
```

> **Зауваження** :
> 
> Метод[PDO::\_\_construct()](pdo.construct.md) завжди кидатиме виняток [PDOException](class.pdoexception.md), если соединение оборвалось, независимо от установленного значения\*\*`PDO::ATTR_ERRMODE`\*\*

**Приклад #2 Створення екземпляра класу PDO та встановлення режиму обробки помилок у конструкторі**

```php
<?php
$dsn = 'mysql:dbname=test;host=127.0.0.1';
$user = 'googleguy';
$password = 'googleguy';

$dbh = new PDO($dsn, $user, $password, array(PDO::ATTR_ERRMODE => PDO::ERRMODE_WARNING));

// Следующий запрос приводит к ошибке уровня E_WARNING вместо исключения (когда таблица не существует)
$dbh->query("SELECT wrongcolumn FROM wrongtable");
?>
```

Результат виконання наведеного прикладу:

```
Warning: PDO::query(): SQLSTATE[42S02]: Base table or view not found: 1146 Table 'test.wrongtable' doesn't exist in
/tmp/pdo_test.php on line 9
```
