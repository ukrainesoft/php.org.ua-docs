---
navigation:
  - sqlite3.enableexceptions.md: '« SQLite3::enableExceptions'
  - sqlite3.exec.md: 'SQLite3::exec »'
  - index.md: PHP Manual
  - class.sqlite3.md: SQLite3
title: 'SQLite3::escapeString'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SQLite3::escapeString

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SQLite3::escapeString — Повертає правильно екранований рядок

### Опис

```methodsynopsis
public static SQLite3::escapeString(string $string): string
```

Повертає правильно екранований термін для безпечного включення до SQL-інструкції.

**Увага**

Ця функція (поки що) небезпечна для обробки даних у двійковій формі!

Для обробки полів типу BLOB, які можуть містити символ NUL, замість цієї функції використовуйте [SQLite3Stmt::bindParam()](sqlite3stmt.bindparam.md)

### Список параметрів

`string`

Рядок для обробки

### Значення, що повертаються

Повертає правильно екранований термін, який може бути безпечно використаний в SQL-інструкції.

### Примітки

**Увага**

[addslashes()](function.addslashes.md) *НЕ* повинен використовуватися для екранування ваших рядків у запитах SQLite; це буде призводити до несподіваних результатів при вилученні ваших даних.
