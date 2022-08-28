Перевіряє, чи розпочато транзакцію

-   [« PDO::getAvailableDrivers](pdo.getavailabledrivers.html)
    
-   [PDO::lastInsertId »](pdo.lastinsertid.html)
    
-   [PHP Manual](index.html)
    
-   [PDO](class.pdo.html)
    
-   Перевіряє, чи розпочато транзакцію
    

# PDO::inTransaction

(PHP 5> = 5.3.3, Bundled pdopgsql, PHP 7, PHP 8)

PDO::inTransaction — Перевіряє, чи розпочато транзакцію

### Опис

```methodsynopsis
public PDO::inTransaction(): bool
```

Перевіряє, чи активна транзакція в драйвері. Цей метод працює тільки для драйверів бази даних, які підтримують транзакції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**якщо транзакція в даний момент активна і **`false`**, якщо ні.