Повертає значення вказаного параметра конфігурації

-   [« sqlsrvfreestmt](function.sqlsrv-free-stmt.html)
    
-   [sqlsrvgetfield »](function.sqlsrv-get-field.html)
    
-   [PHP Manual](index.html)
    
-   [Функції SQLSRV](ref.sqlsrv.html)
    
-   Повертає значення вказаного параметра конфігурації
    

# sqlsrvgetconfig

(No version information available, might only be in Git)

sqlsrvgetconfig — Повертає значення вказаного параметра конфігурації

### Опис

```methodsynopsis
sqlsrv_get_config(string $setting): mixed
```

Повертає значення вказаного параметра конфігурації.

### Список параметрів

`setting`

Назва параметра, для якого повертається значення. Список настроюваних параметрів дивіться в розділі [sqlsrvconfigure()](function.sqlsrv-configure.html)

### Значення, що повертаються

Повертає значення вказаного параметра. Якщо вказано неправильний параметр, повертається **`false`**

### Дивіться також

-   [sqlsrvconfigure()](function.sqlsrv-configure.html) - Змінює конфігурацію обробки помилок драйвера та ведення журналу