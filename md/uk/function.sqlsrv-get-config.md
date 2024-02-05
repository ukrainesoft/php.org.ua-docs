---
navigation:
  - function.sqlsrv-free-stmt.md: « sqlsrv\_free\_stmt
  - function.sqlsrv-get-field.md: sqlsrv\_get\_field »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrv\_get\_config
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqlsrv\_get\_config

(No version information available, might only be in Git)

sqlsrv\_get\_config — Повертає значення вказаного параметра конфігурації

### Опис

```methodsynopsis
sqlsrv_get_config(string $setting): mixed
```

Повертає значення вказаного параметра конфігурації.

### Список параметрів

`setting`

Назва параметра, для якого повертається значення. Список настроюваних параметрів дивіться в розділі [sqlsrv\_configure()](function.sqlsrv-configure.md)

### Значення, що повертаються

Повертає значення вказаного параметра. Якщо вказано неправильний параметр, повертається **`false`**

### Дивіться також

-   [sqlsrv\_configure()](function.sqlsrv-configure.md) \- Змінює конфігурацію обробки помилок драйвера та ведення журналу
