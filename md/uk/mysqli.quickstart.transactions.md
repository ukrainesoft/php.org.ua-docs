API підтримка транзакцій

-   [« Множественные запросы](mysqli.quickstart.multiple-statement.html)
    
-   [Метаданные »](mysqli.quickstart.metadata.html)
    
-   [PHP Manual](index.html)
    
-   [Краткое руководство](mysqli.quickstart.html)
    
-   API підтримка транзакцій
    

## API підтримка транзакцій

Підтримка транзакцій в СУБД MySQL залежить від використовуваного двигуна сховища даних. Починаючи з MySQL 5.5, за замовчуванням використовується двигун InnoDB. InnoDB повністю підтримує модель транзакцій ACID.

Транзакції можна керувати як засобами SQL, так і викликами API-функцій. Для увімкнення та вимкнення режиму автофіксації змін (`autocommit`) рекомендується користуватися API функціями.

**Приклад #1 Встановлення режиму автофіксації (`autocommit`) засобами SQL та функціями API**

```php
<?php
mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("example.com", "user", "password", "database");

/* Рекомендуется управлять настройками транзакций средствами API */
$mysqli->autocommit(false);

/* Не будет распознаваться и учитываться плагинами репликации и балансировки нагрузки */
$mysqli->query('SET AUTOCOMMIT = 0');
```

Додаткові служби сервера, такі як плагіни реплікації та балансування навантаження, можуть відстежувати виклики API-функцій. Плагін реплікації може повідомляти балансувальнику навантаження про запущену транзакцію, якщо ця транзакція обслуговується API-функціями. Сервер не зможе розподіляти навантаження між репліками бази, якщо зміна режиму автофіксації (`autocommit`), фіксація та відкат транзакцій здійснюються SQL-запитами.

**Приклад #2 Фіксація та відкат**

```php
<?php
mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("example.com", "user", "password", "database");
$mysqli->autocommit(false);

$mysqli->query("INSERT INTO test(id) VALUES (1)");
$mysqli->rollback();

$mysqli->query("INSERT INTO test(id) VALUES (2)");
$mysqli->commit();
```

Слід зазначити, що MySQL сервер не може відкотити результати всіх запитів. Деякі зміни фіксуються неявно.

*Дивіться також*

-   [mysqli::autocommit()](mysqli.autocommit.html)
-   [mysqli::begin\_transaction()](mysqli.begin-transaction.html)
-   [mysqli::commit()](mysqli.commit.html)
-   [mysqli::rollback()](mysqli.rollback.html)