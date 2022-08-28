Видаляє всі поточні параметри

-   [« SQLite3Stmt::bindValue](sqlite3stmt.bindvalue.html)
    
-   [SQLite3Stmt::close »](sqlite3stmt.close.html)
    
-   [PHP Manual](index.html)
    
-   [SQLite3Stmt](class.sqlite3stmt.html)
    
-   Видаляє всі поточні параметри
    

# SQLite3Stmt::clear

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SQLite3Stmt::clear — Видалення всіх поточних параметрів.

### Опис

```methodsynopsis
public SQLite3Stmt::clear(): bool
```

Видаляє всі поточні параметри (встановлює їх на значення **`null`**

**Застереження**

Метод необхідно використовувати з [SQLite3Stmt::reset()](sqlite3stmt.reset.html). Якщо використовується один, будь-який виклик [SQLite3Stmt::bindValue()](sqlite3stmt.bindvalue.html) або [SQLite3Stmt::bindParam()](sqlite3stmt.bindparam.html) не матиме жодного ефекту, і всі прив'язані параметри матимуть значення **`null`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного очищення прив'язаних параметрів та **`false`** у разі виникнення помилки.