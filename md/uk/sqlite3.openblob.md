---
navigation:
  - sqlite3.open.md: '« SQLite3::open'
  - sqlite3.prepare.md: 'SQLite3::prepare »'
  - index.md: PHP Manual
  - class.sqlite3.md: SQLite3
title: 'SQLite3::openBlob'
---
# SQLite3::openBlob

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SQLite3::openBlob — Відкриває ресурс потоку для читання BLOB

### Опис

```methodsynopsis
public SQLite3::openBlob(    string $table,    string $column,    int $rowid,    string $database = "main",    int $flags = SQLITE3_OPEN_READONLY): resource|false
```

Відкриває потоковий ресурс для читання або запису BLOB, який буде обраний:

SELECT `column` FROM `database``table` WHERE rowid = `rowid`

> **Зауваження**: Неможливо змінити розмір BLOB шляхом запису до потоку. Натомість необхідно виконати запит UPDATE, можливо, використовуючи SQLite-функцію zeroblob(), щоб задати бажаний розмір BLOB.

### Список параметрів

`table`

Назва таблиці.

`column`

Назва стовпця.

`rowid`

Ідентифікатор рядка.

`database`

Символічна назва бази даних

`flags`

Або **`SQLITE3_OPEN_READONLY`**, або **`SQLITE3_OPEN_READWRITE`**, щоб відкрити потік тільки для читання або для читання та запису відповідно.

### Значення, що повертаються

Повертає ресурс потоку або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Доданий параметр `flags`, Що дозволяє записати BLOB; раніше підтримувалося лише читання. |

### Приклади

**Приклад #1 Приклад використання **SQLite3::openBlob()****

```php
<?php
$conn = new SQLite3(':memory:');
$conn->exec('CREATE TABLE test (text text)');
$conn->exec("INSERT INTO test VALUES ('Lorem ipsum')");
$stream = $conn->openBlob('test', 'text', 1);
echo stream_get_contents($stream);
fclose($stream); // обязательно, иначе на следующей строке произойдёт ошибка
$conn->close();
?>
```

Результат виконання цього прикладу:

```
Lorem ipsum
```

**Приклад #2 Покроковий запис BLOB**

```php
<?php
$conn = new SQLite3(':memory:');
$conn->exec('CREATE TABLE test (text text)');
$conn->exec("INSERT INTO test VALUES (zeroblob(36))");
$stream = $conn->openBlob('test', 'text', 1, 'main', SQLITE3_OPEN_READWRITE);
for ($i = 0; $i < 3; $i++) {
    fwrite($stream,  "Lorem ipsum\n");
}
fclose($stream);
echo $conn->querySingle("SELECT text FROM test");
$conn->close();
?>
```

Результат виконання цього прикладу:

```
Lorem ipsum
Lorem ipsum
Lorem ipsum
```
