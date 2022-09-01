---
navigation:
  - class.sqlite3result.html: « SQLite3Result
  - sqlite3result.columntype.html: 'SQLite3Result::columnType »'
  - index.html: PHP Manual
  - class.sqlite3result.html: SQLite3Result
title: 'SQLite3Result::columnName'
---
# SQLite3Result::columnName

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SQLite3Result::columnName — >Повертає ім'я n-ого стовпця

### Опис

```methodsynopsis
public SQLite3Result::columnName(int $column): string|false
```

Повертає ім'я стовпця, зазначеного в `column_number`. Зверніть увагу, що ім'я стовпця результату – це значення пропозиції `AS` для цього стовпця, якщо є пропозиція `AS`. Якщо пропозиція `AS` відсутня, тоді ім'я шпальти не вказано і може змінитися з одного випуску libsqlite3 на інший.

### Список параметрів

`column`

Номер стовпця, починаючи з нуля.

### Значення, що повертаються

Повертає ім'я (string) стовпця, вказаного в `column`
