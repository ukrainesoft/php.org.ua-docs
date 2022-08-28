Скидає підготовлений запит

-   [« SQLite3Stmt::readOnly](sqlite3stmt.readonly.html)
    
-   [SQLite3Result »](class.sqlite3result.html)
    
-   [PHP Manual](index.html)
    
-   [SQLite3Stmt](class.sqlite3stmt.html)
    
-   Скидає підготовлений запит
    

# SQLite3Stmt::reset

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SQLite3Stmt::reset — Скидає підготовлений запит

### Опис

```methodsynopsis
public SQLite3Stmt::reset(): bool
```

Скидає підготовлений запит до стану до його виконання. Після скидання всі прив'язки залишаються незмінними.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у випадку, якщо підготовлений запит був успішно скинутий або **`false`** у разі виникнення помилки.