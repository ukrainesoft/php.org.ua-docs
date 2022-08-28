Звільняє ресурси, які займає курсор або SQL-вираз.

-   [« oci\_free\_descriptor](function.oci-free-descriptor.html)
    
-   [oci\_get\_implicit\_resultset »](function.oci-get-implicit-resultset.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8 Функции](ref.oci8.html)
    
-   Звільняє ресурси, які займає курсор або SQL-вираз.
    

# ocifreestatement

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocifreestatement — Звільняє ресурси, які займає курсор або SQL-вираз.

### Опис

```methodsynopsis
oci_free_statement(resource $statement): bool
```

Звільняє всі ресурси, що займаються курсором або SQL-виразом, яке повернуто функцією [oci\_parse()](function.oci-parse.html) або отримано від сервера Oracle.

### Список параметрів

`statement`

Допустимий ідентифікатор OCI-виразу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.