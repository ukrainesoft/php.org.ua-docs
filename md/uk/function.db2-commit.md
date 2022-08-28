Підтверджує транзакцію

-   [« db2\_columns](function.db2-columns.html)
    
-   [db2\_conn\_error »](function.db2-conn-error.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IBM DB2](ref.ibm-db2.html)
    
-   Підтверджує транзакцію
    

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

Змінна, що містить активний ресурс підключення, отриманий за допомогою [db2\_connect()](function.db2-connect.html) або [db2\_pconnect()](function.db2-pconnect.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [db2\_autocommit()](function.db2-autocommit.html) - Повертає або встановлює режим автопідтвердження транзакцій для з'єднання
-   [db2\_rollback()](function.db2-rollback.html) - Відкочує транзакцію