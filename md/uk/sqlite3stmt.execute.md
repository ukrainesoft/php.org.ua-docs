---
navigation:
  - sqlite3stmt.construct.md: '« SQLite3Stmt::construct'
  - sqlite3stmt.getsql.md: 'SQLite3Stmt::getSQL »'
  - index.md: PHP Manual
  - class.sqlite3stmt.md: SQLite3Stmt
title: 'SQLite3Stmt::execute'
---
# SQLite3Stmt::execute

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SQLite3Stmt::execute — Виконує підготовлений запит і повертає об'єкт із результуючим набором

### Опис

```methodsynopsis
public SQLite3Stmt::execute(): SQLite3Result|false
```

Виконує підготовлений запит та повертає об'єкт із результуючим набором.

**Застереження**

Об'єкти результуючого набору, отримані при виклику цього методу для одного і того ж об'єкта підготовленого запиту, не є незалежними, а використовують одну й ту саму базову структуру. Тому рекомендується викликати [SQLite3Result::finalize()](sqlite3result.finalize.md), перш ніж викликати **SQLite3Stmt::execute()** на тому самому об'єкті підготовленого запиту знову.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [SQLite3Result](class.sqlite3result.md) у разі успішного виконання підготовленого запиту та **`false`** у разі виникнення помилки.

### Дивіться також

-   [SQLite3::prepare()](sqlite3.prepare.md) - готує SQL-запит для виконання
-   [SQLite3Stmt::bindValue()](sqlite3stmt.bindvalue.md) - Зв'язує значення параметра зі змінною підготовленого запиту
-   [SQLite3Stmt::bindParam()](sqlite3stmt.bindparam.md) - Зв'язує параметр із змінною підготовленого запиту
