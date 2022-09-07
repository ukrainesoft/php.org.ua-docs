---
navigation:
  - sqlite3.backup.md: '« SQLite3::backup'
  - sqlite3.changes.md: 'SQLite3::changes »'
  - index.md: PHP Manual
  - class.sqlite3.md: SQLite3
title: 'SQLite3::busyTimeout'
---
# SQLite3::busyTimeout

(PHP 5> = 5.3.3, PHP 7, PHP 8)

SQLite3::busyTimeout — Встановити обробник "зайнято" на з'єднання

### Опис

```methodsynopsis
public SQLite3::busyTimeout(int $milliseconds): bool
```

Встановлює обробник, який спатиме доти, доки БД не заблокується або поки не закінчиться час очікування.

### Список параметрів

`milliseconds`

Мілісекунди. Установка рівним 0 або негативного значення призведе до відключення вже встановленого оброблювача.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
