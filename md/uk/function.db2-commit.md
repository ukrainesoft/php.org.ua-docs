---
navigation:
  - function.db2-columns.html: « db2columns
  - function.db2-conn-error.html: db2connerror »
  - index.html: PHP Manual
  - ref.ibm-db2.html: Функції IBM DB2
title: db2commit
---
# db2commit

(PECL ibmdb2> = 1.0.0)

db2commit - Підтверджує транзакцію

### Опис

```methodsynopsis
db2_commit(resource $connection): bool
```

Підтверджує поточну транзакцію на зазначеному з'єднанні та починає нову. За промовчанням, в PHP, використовується автопідтвердження транзакцій, так що функція **db2commit()** потрібна лише в тому випадку, якщо ви примусово відключили автопідтвердження транзакцій для з'єднання.

### Список параметрів

`connection`

Змінна, що містить активний ресурс підключення, отриманий за допомогою [db2connect()](function.db2-connect.html) або [db2pconnect()](function.db2-pconnect.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [db2autocommit()](function.db2-autocommit.html) - Повертає або встановлює режим автопідтвердження транзакцій для з'єднання
-   [db2rollback()](function.db2-rollback.html) - Відкочує транзакцію
