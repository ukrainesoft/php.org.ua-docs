---
navigation:
  - sqlite3.resources.md: « Типи ресурсів
  - class.sqlite3.md: SQLite3 »
  - index.md: PHP Manual
  - book.sqlite3.md: SQLite3
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**`SQLITE3_ASSOC`**(int)

Вказує на те, що [Sqlite3Result::fetchArray()](sqlite3result.fetcharray.md) метод повинен повернути масив, індексований на ім'я стовпця у відповідний набір результатів.

**`SQLITE3_NUM`**(int)

Вказує на те, що [Sqlite3Result::fetchArray()](sqlite3result.fetcharray.md) метод повинен повернути масив, індексований за номером стовпця у відповідний набір результатів, починаючи із стовпця 0.

**`SQLITE3_BOTH`**(int)

Вказує на те, що [Sqlite3Result::fetchArray()](sqlite3result.fetcharray.md) метод повинен повернути масив, індексований на ім'я стовпця та його номеру у відповідний набір результатів, починаючи зі стовпця 0.

**`SQLITE3_INTEGER`**(int)

Представляє клас зберігання типу SQLite3 INTEGER.

**`SQLITE3_FLOAT`**(int)

Представляє клас зберігання типу SQLite3 REAL (FLOAT).

**`SQLITE3_TEXT`**(int)

Представляє клас зберігання типу SQLite3 TEXT.

**`SQLITE3_BLOB`**(int)

Представляє клас зберігання типу SQLite3 BLOB.

**`SQLITE3_NULL`**(int)

Представляє клас зберігання типу SQLite3 NULL.

**`SQLITE3_OPEN_READONLY`**(int)

Вказує на те, що база даних SQLite3 доступна лише для читання.

**`SQLITE3_OPEN_READWRITE`**(int)

Вказує на те, що база даних SQLite3 доступна як для читання, так і для запису.

**`SQLITE3_OPEN_CREATE`**(int)

Вказує на те, що файл бази даних SQLite3 буде створений, якщо він ще не існує.

**`SQLITE3_DETERMINISTIC`**(int)

Вказує, що функція створена **SQLite3::sqliteCreateFunction()** детермінована. Тобто. вона завжди повертає однаковий результат для однакових вхідних даних в одному виразі SQL. (Доступно з PHP 7.1.4.)
