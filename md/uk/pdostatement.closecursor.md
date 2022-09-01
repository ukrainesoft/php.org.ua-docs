---
navigation:
  - pdostatement.bindvalue.md: '« PDOStatement::bindValue'
  - pdostatement.columncount.md: 'PDOStatement::columnCount »'
  - index.md: PHP Manual
  - class.pdostatement.md: PDOStatement
title: 'PDOStatement::closeCursor'
---
# PDOStatement::closeCursor

(PHP 5> = 5.1.0, PHP 7, PHP 8, PECL pdo> = 0.9.0)

PDOStatement::closeCursor — Закриває курсор, переводячи запит у стан готовності до повторного запуску

### Опис

```methodsynopsis
public PDOStatement::closeCursor(): bool
```

**PDOStatement::closeCursor()** звільняє з'єднання із сервером, даючи можливість запускати інші SQL-запити. Метод залишає запит у стані готовності до повторного запуску.

Цей метод корисний при використанні драйверів баз даних, які не дозволяють запустити PDOStatement, доки попередній об'єкт PDOStatement не вибере всі дані з результуючого набору. Якщо це обмеження поширюється на драйвер, буде викликана помилка порушення послідовності запитів (out-of-sequence error).

**PDOStatement::closeCursor()** може бути реалізований як додатковий метод конкретного драйвера (що дозволяє досягти максимальної ефективності роботи), або як внутрішній метод PDO, якщо такої функції в драйвері немає. Реалізація внутрішнього методу PDO семантично схожа з наведеною нижче:

```php
<?php
do {
    while ($stmt->fetch())
        ;
    if (!$stmt->nextRowset())
        break;
} while (true);
?>
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **PDOStatement::closeCursor()****

У наведеному прикладі, об'єкт PDOStatement $stmt повертає кілька рядків, проте програма зчитує лише перший з них, залишаючи об'єкт PDOStatement у стані, коли є ще невибрані рядки. Щоб бути впевненим у тому, що програма буде працювати з усіма драйверами баз даних, автор додав виклик методу **PDOStatement::closeCursor()** об'єкта $stmt перед тим, як запустити інший запит PDOStatement $otherStmt.

```php
<?php
/* Создание объекта PDOStatement */
$stmt = $dbh->prepare('SELECT foo FROM bar');

/* Создание другого объекта PDOStatement */
$otherStmt = $dbh->prepare('SELECT foobaz FROM foobar');

/* Выполнение первого запроса */
$stmt->execute();

/* Выборка только первой строки результирующего набора первого запроса */
$stmt->fetch();

/* Следующий вызов closeCursor() может быть обязательным для некоторых драйверов */
$stmt->closeCursor();

/* теперь можно запускать второй запрос */
$otherStmt->execute();
?>
```

### Дивіться також

-   [PDOStatement::execute()](pdostatement.execute.md) - Запускає підготовлений запит на виконання
