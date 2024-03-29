---
navigation:
  - function.oci-error.md: « oci\_error
  - function.oci-fetch-all.md: oci\_fetch\_all »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_execute
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_execute

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_execute — Виконує підготовлений вираз

### Опис

```methodsynopsis
oci_execute(resource $statement, int $mode = OCI_COMMIT_ON_SUCCESS): bool
```

Виконує підготовлений вираз `statement`, створене за допомогою функції [oci\_parse()](function.oci-parse.md)

Відразу після виконання такого вираження `INSERT`, за промовчанням всі дані одразу будуть збережені в базі даних. Для подібних виразів `SELECT`, виконується лише логіка запиту. Результат же запиту можна отримати пізніше в PHP за допомогою подібних функцій [oci\_fetch\_array()](function.oci-fetch-array.md)

Кожне підготовлене вираз може бути виконано кілька разів для економії витратах від повторної підготовки запиту. Це найчастіше застосовується для виразів `INSERT`, коли до них прив'язані дані за допомогою [oci\_bind\_by\_name()](function.oci-bind-by-name.md)

### Список параметрів

`statement`

Правильне підготовлене вираження OCI.

`mode`

Необов'язковий другий параметр з одним із наступних значень:

**Режим виконання**

| Константа | Опис |
| --- | --- |
| **`OCI_COMMIT_ON_SUCCESS`** | Автоматично зберігати всі незбережені зміни, здійснені за поточну сесію у разі успішного виконання виразу. Цей режим встановлено за замовчуванням. |
| **`OCI_DESCRIBE_ONLY`** | Робить доступними метадані запити для подібних функцій [oci\_field\_name()](function.oci-field-name.md), але створює результат виконання висловлювання. Будь-яке подальше отримання даних, наприклад, за допомогою [oci\_fetch\_array()](function.oci-fetch-array.md) не буде зроблено. |
| **`OCI_NO_AUTO_COMMIT`** | Не зберігати автоматично зміни. |

Использование режима\*\*`OCI_NO_AUTO_COMMIT`\*\* відкриває чи продовжує транзакцію. Ця транзакція автоматично відкочується під час закриття з'єднання або завершення скрипту. Використовуйте [oci\_commit()](function.oci-commit.md) для завершення транзакції та [oci\_rollback()](function.oci-rollback.md) для її скасування.

При вставці та оновленні даних рекомендується використання транзакцій для реляційної цілісності даних та для покращення продуктивності.

Якщо для якогось виразу використовується режим **`OCI_NO_AUTO_COMMIT`**, і згодом не використовуються [oci\_commit()](function.oci-commit.md) або [oci\_rollback()](function.oci-rollback.md), то OCI8 буде виконувати відкат при завершенні скрипта навіть якщо дані не були змінені. Для уникнення непотрібних відкатів більшість скриптів не використовують режим **`OCI_NO_AUTO_COMMIT`** для запитів або PL/SQL. Будьте уважні, щоб забезпечити належну узгодженість транзакцій під час використання **oci\_execute()** із різними режимами в одному скрипті.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1**oci\_execute()\*\* під час виконання запитів\*\*

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');

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

**Приклад #2**oci\_execute()\*\* без вказівки певного режиму\*\*

```php
<?php

// Перед выполнением создайте таблицу:
//   CREATE TABLE MYTABLE (col1 NUMBER);

$conn = oci_connect('hr', 'welcome', 'localhost/XE');

$stid = oci_parse($conn, 'INSERT INTO mytab (col1) VALUES (123)');

oci_execute($stid); // Строка сохранена и становится видимой для других пользователей

?>
```

**Приклад #3**oci\_execute()**с**`OCI_NO_AUTO_COMMIT`\*\*\*\*

```php
<?php

// Перед выполнением создайте таблицу:
//   CREATE TABLE MYTABLE (col1 NUMBER);

$conn = oci_connect('hr', 'welcome', 'localhost/XE');

$stid = oci_parse($conn, 'INSERT INTO mytab (col1) VALUES (:bv)');
oci_bind_by_name($stid, ':bv', $i, 10);
for ($i = 1; $i <= 5; ++$i) {
    oci_execute($stid, OCI_NO_AUTO_COMMIT);
}
oci_commit($conn);  // сохранение все новых значений: 1, 2, 3, 4, 5

?>
```

**Приклад #4**oci\_execute()\*\* з різними режимами\*\*

```php
<?php

// Перед выполнением создайте таблицу:
//   CREATE TABLE MYTABLE (col1 NUMBER);

$conn = oci_connect('hr', 'welcome', 'localhost/XE');

$stid = oci_parse($conn, 'INSERT INTO mytab (col1) VALUES (123)');
oci_execute($stid, OCI_NO_AUTO_COMMIT);  // data not committed

$stid = oci_parse($conn, 'INSERT INTO mytab (col1) VALUES (456)');
oci_execute($stid);  // commits both 123 and 456 values

?>
```

**Приклад #5**oci\_execute()**с**`OCI_DESCRIBE_ONLY`\*\*\*\*

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');

$stid = oci_parse($conn, 'SELECT * FROM locations');
oci_execute($s, OCI_DESCRIBE_ONLY);
for ($i = 1; $i <= oci_num_fields($stid); ++$i) {
    echo oci_field_name($stid, $i) . "<br>\n";
}

?>
```

### Примітки

> **Зауваження** :
> 
> Транзакції автоматично відкочуються під час закриття з'єднання або завершення виконання скрипту. Примусово викликайте [oci\_commit()](function.oci-commit.md) для завершення транзакції.
> 
> Будь-який виклик **oci\_execute()**, який примусово використовує **`OCI_COMMIT_ON_SUCCESS`** або за умовчанням завершуватиме будь-яку попередню незакриту транзакцію.
> 
> Будь-який вираз Oracle DDL подібний `CREATE`или`DROP` буде автоматично завершувати будь-яку. незакриту транзакцію.

> **Зауваження** :
> 
> Оскільки функція **oci\_execute()** зазвичай відправляє вирази до бази даних, то **oci\_execute()** може знайти деякі незначні синтаксичні помилки, коли локальна [oci\_parse()](function.oci-parse.md)их не находит.

### Дивіться також

-   [oci\_parse()](function.oci-parse.md) \- готує запит до виконання
