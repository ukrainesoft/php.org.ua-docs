---
navigation:
  - class.sqlite3result.md: « SQLite3Result
  - sqlite3result.columntype.md: 'SQLite3Result::columnType »'
  - index.md: PHP Manual
  - class.sqlite3result.md: SQLite3Result
title: 'SQLite3Result::columnName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SQLite3Result::columnName

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SQLite3Result::columnName —>Повертає ім'я n-ого стовпця

### Опис

```methodsynopsis
public SQLite3Result::columnName(int $column): string|false
```

Повертає ім'я стовпця, зазначеного в `column_number`. Зверніть увагу, що ім'я стовпця результату – це значення пропозиції `AS` для цього стовпця, якщо є пропозиція `AS`Если предложение`AS` відсутня, тоді ім'я стовпця не вказано і може змінитися з одного випуску libsqlite3 на інший.

### Список параметрів

`column`

Номер стовпця, починаючи з нуля.

### Значення, що повертаються

Повертає ім'я (string) стовпця, вказаного в `column`
