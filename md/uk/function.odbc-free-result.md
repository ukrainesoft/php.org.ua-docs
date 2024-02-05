---
navigation:
  - function.odbc-foreignkeys.md: « odbc\_foreignkeys
  - function.odbc-gettypeinfo.md: odbc\_gettypeinfo »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_free\_result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_free\_result

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_free\_result — Звільняє ресурси, пов'язані з результатом

### Опис

```methodsynopsis
odbc_free_result(resource $statement): bool
```

Визволяє ресурси, пов'язані з результатом.

**odbc\_free\_result()** потрібно викликати лише в тому випадку, якщо під час роботи вашого скрипта використовується занадто багато пам'яті. Вся пам'ять, що зберігає результат, буде автоматично звільнена після завершення сценарію.

### Список параметрів

`statement`

Ідентифікатор результату.

### Значення, що повертаються

Завжди повертає **`true`**

### Примітки

> **Зауваження** :
> 
> Якщо автоматична фіксація вимкнена (див. . [odbc\_autocommit()](function.odbc-autocommit.md)), и**odbc\_free\_result()** викликається перед фіксацією, всі транзакції, що очікують, відкочуються.
