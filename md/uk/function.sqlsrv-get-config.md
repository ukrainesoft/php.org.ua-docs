---
navigation:
  - function.sqlsrv-free-stmt.html: « sqlsrvfreestmt
  - function.sqlsrv-get-field.html: sqlsrvgetfield »
  - index.html: PHP Manual
  - ref.sqlsrv.html: Функції SQLSRV
title: sqlsrvgetconfig
---
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

Назва параметра, для якого повертається значення. Список настроюваних параметрів дивіться в розділі [sqlsrvconfigure()](function.sqlsrv-configure.md)

### Значення, що повертаються

Повертає значення вказаного параметра. Якщо вказано неправильний параметр, повертається **`false`**

### Дивіться також

-   [sqlsrvconfigure()](function.sqlsrv-configure.md) - Змінює конфігурацію обробки помилок драйвера та ведення журналу
