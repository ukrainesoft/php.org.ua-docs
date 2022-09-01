---
navigation:
  - function.oci-result.html: « ociresult
  - function.oci-server-version.html: ociserverversion »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функции
title: ocirollback
---
# ocirollback

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocirollback - Відкочує транзакції, що очікують обробки

### Опис

```methodsynopsis
oci_rollback(resource $connection): bool
```

Ця функція відкочує всі незафіксовані зміни з'єднання Oracle `connection` та завершує транзакцію. Вона також звільняє всі блокування. Видаляються всі Oracle `SAVEPOINTS`

Транзакція починається при першому SQL-запиті, який змінює дані, який був запущений за допомогою функції [ociexecute()](function.oci-execute.html) та прапор **`OCI_NO_AUTO_COMMIT`**. Наступні зміни даних від інших запитів також стають частиною цієї транзакції. Зміни, зроблені в транзакції, є тимчасовими доти, доки транзакція не буде зафіксована або буде здійснено її відкат. Інші користувачі бази даних не зможуть побачити зміни до їхньої фіксації.

При вставці або оновленні даних рекомендується використовувати транзакції для збереження цілісності даних та збільшення продуктивності.

### Список параметрів

`connection`

Ідентифікатор з'єднання Oracle, отриманий із функцій [ociconnect()](function.oci-connect.html) [ocipconnect()](function.oci-pconnect.html) або [ocinewconnect()](function.oci-new-connect.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ocirollback()****

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
if (!r) {
    $e = oci_error($conn);
    trigger_error(htmlentities($e['message']), E_USER_ERROR);
}

?>
```

**Приклад #2 Приклад використання відкату до `SAVEPOINT`**

```php
<?php
$stid = oci_parse($conn, 'UPDATE mytab SET id = 1111');
oci_execute($stid, OCI_NO_AUTO_COMMIT);

// Создаём точку сохранения
$stid = oci_parse($conn, 'SAVEPOINT mysavepoint');
oci_execute($stid, OCI_NO_AUTO_COMMIT);

$stid = oci_parse($conn, 'UPDATE mytab SET id = 2222');
oci_execute($stid, OCI_NO_AUTO_COMMIT);

// Явно используем SQL-запрос для отката к точке сохранения
$stid = oci_parse($conn, 'ROLLBACK TO SAVEPOINT mysavepoint');
oci_execute($stid, OCI_NO_AUTO_COMMIT);

oci_commit($conn);  // mytab теперь содержит id равные 1111
?>
```

### Примітки

> **Зауваження**
> 
> Транзакції будуть автоматично відкачені під час закриття з'єднання або закінчення скрипту (залежно від того, що станеться раніше). Для фіксації транзакції необхідно явно викликати функцію [ocicommit()](function.oci-commit.html)
> 
> Усі виклики [ociexecute()](function.oci-execute.html), явно або за замовчуванням, що використовують режим **`OCI_COMMIT_ON_SUCCESS`** зафіксують будь-яку попередню незафіксовану транзакцію.
> 
> Будь-який DDL-запит Oracle, такий як `CREATE` або `DROP` автоматично фіксує будь-яку незафіксовану транзакцію.

### Дивіться також

-   [ocicommit()](function.oci-commit.html) - підтверджує транзакцію бази даних
-   [ociexecute()](function.oci-execute.html) - Виконує підготовлений вираз
