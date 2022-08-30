Звільняє ресурси, які займає курсор або SQL-вираз.

-   [« ocifreedescriptor](function.oci-free-descriptor.html)
    
-   [ocigetimplicitresultset »](function.oci-get-implicit-resultset.html)
    
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

Звільняє всі ресурси, що займаються курсором або SQL-виразом, яке повернуто функцією [ociparse()](function.oci-parse.html) або отримано від сервера Oracle.

### Список параметрів

`statement`

Допустимий ідентифікатор OCI-виразу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.