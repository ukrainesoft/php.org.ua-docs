Підтверджує транзакцію бази даних

-   [« oci\_close](function.oci-close.html)
    
-   [oci\_connect »](function.oci-connect.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8 Функции](ref.oci8.html)
    
-   Підтверджує транзакцію бази даних
    

# ocicommit

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocicommit — Підтверджує транзакцію бази даних

### Опис

```methodsynopsis
oci_commit(resource $connection): bool
```

Підтверджує транзакцію з'єднання `connection`. Підтвердження завершує поточну транзакцію та робить усі зміни постійними. Вона також звільняє всі блокування.

Транзакція починається при першому SQL-запиті, який змінює дані, який був запущений за допомогою функції [oci\_execute()](function.oci-execute.html) та прапор **`OCI_NO_AUTO_COMMIT`**. Наступні зміни даних від інших запитів також стають частиною цієї транзакції. Зміни, зроблені в транзакції, є тимчасовими доти, доки транзакція не буде зафіксована або поки не буде здійснено її відкат. Інші користувачі бази даних не зможуть побачити зміни до їх підтвердження.

При вставці або оновленні даних рекомендується використовувати транзакції для збереження цілісності даних та збільшення продуктивності.

### Список параметрів

`connection`

Ідентифікатор з'єднання Oracle, отриманий із функцій [oci\_connect()](function.oci-connect.html) [oci\_pconnect()](function.oci-pconnect.html) або [oci\_new\_connect()](function.oci-new-connect.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ocicommit()****

```php
<?php

// Вставка в несколько таблиц, откат изменений в случае возникновения ошибки

$conn = oci_connect('hr', 'welcome', 'localhost/XE');

$stid = oci_parse($conn, "INSERT INTO mysalary (id, name) VALUES (1, 'Chris')");

// Флаг OCI_NO_AUTO_COMMIT сообщает Oracle не фиксировать запрос INSERT при его поступлении
// Для PHP <= 5.3.1 используйте OCI_DEFAULT, эти два флага эквивалентны
$r = oci_execute($stid, OCI_NO_AUTO_COMMIT);
if (!$r) {
    $e = oci_error($stid);
    trigger_error(htmlentities($e['message']), E_USER_ERROR);
}

$stid = oci_parse($conn, 'INSERT INTO myschedule (startday) VALUES (12)');
$r = oci_execute($stid, OCI_NO_AUTO_COMMIT);
if (!$r) {
    $e = oci_error($stid);
    oci_rollback($conn);  // откат изменений из обоих таблиц
    trigger_error(htmlentities($e['message']), E_USER_ERROR);
}

// Фиксация изменений в обоих таблицах
$r = oci_commit($conn);
if (!$r) {
    $e = oci_error($conn);
    trigger_error(htmlentities($e['message']), E_USER_ERROR);
}

?>
```

### Примітки

> **Зауваження**
> 
> Транзакції будуть автоматично відкачені під час закриття з'єднання або закінчення скрипту (залежно від того, що станеться раніше). Для підтвердження транзакції необхідно явно викликати функцію **ocicommit()**
> 
> Усі виклики [oci\_execute()](function.oci-execute.html), явно або за замовчуванням, що використовують режим **`OCI_COMMIT_ON_SUCCESS`** зафіксують будь-яку попередню незафіксовану транзакцію.
> 
> Будь-який DDL-запит Oracle, такий як `CREATE` або `DROP` автоматично підтверджує будь-яку незавершену транзакцію.

### Дивіться також

-   [oci\_execute()](function.oci-execute.html) - Виконує підготовлений вираз
-   [oci\_rollback()](function.oci-rollback.html) - Відкочує транзакції, що очікують на обробку