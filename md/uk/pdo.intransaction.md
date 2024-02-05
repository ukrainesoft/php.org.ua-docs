---
navigation:
  - pdo.getavailabledrivers.md: '« PDO::getAvailableDrivers'
  - pdo.lastinsertid.md: 'PDO::lastInsertId »'
  - index.md: PHP Manual
  - class.pdo.md: PDO
title: 'PDO::inTransaction'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDO::inTransaction

(PHP 5 >= 5.3.3, Bundled pdo\_pgsql, PHP 7, PHP 8)

PDO::inTransaction — Перевіряє, чи розпочато транзакцію

### Опис

```methodsynopsis
public PDO::inTransaction(): bool
```

Перевіряє, чи активна транзакція в драйвері. Цей метод працює тільки для драйверів бази даних, які підтримують транзакції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо транзакція на даний момент активна та **`false`**, якщо ні.
