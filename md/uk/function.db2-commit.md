---
navigation:
  - function.db2-columns.md: « db2\_columns
  - function.db2-conn-error.md: db2\_conn\_error »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_commit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_commit

(PECL ibm\_db2 >= 1.0.0)

db2\_commit - Підтверджує транзакцію

### Опис

```methodsynopsis
db2_commit(resource $connection): bool
```

Підтверджує поточну транзакцію на зазначеному з'єднанні та починає нову. За промовчанням, в PHP, використовується автопідтвердження транзакцій, так що функція **db2\_commit()** потрібна лише в тому випадку, якщо ви примусово відключили автопідтвердження транзакцій для з'єднання.

### Список параметрів

`connection`

Змінна, що містить активний ресурс підключення, отриманий за допомогою [db2\_connect()](function.db2-connect.md) або [db2\_pconnect()](function.db2-pconnect.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [db2\_autocommit()](function.db2-autocommit.md) \- Повертає або встановлює режим автопідтвердження транзакцій для з'єднання
-   [db2\_rollback()](function.db2-rollback.md) \- Відкочує транзакцію
