---
navigation:
  - function.odbc-foreignkeys.html: « odbcforeignkeys
  - function.odbc-gettypeinfo.html: odbcgettypeinfo »
  - index.md: PHP Manual
  - ref.uodbc.md: Функции ODBC
title: odbcfreeresult
---
# odbcfreeresult

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcfreeresult — Звільняє ресурси, пов'язані з результатом

### Опис

```methodsynopsis
odbc_free_result(resource $statement): bool
```

Визволяє ресурси, пов'язані з результатом.

**odbcfreeresult()** потрібно викликати лише в тому випадку, якщо під час роботи вашого скрипта використовується занадто багато пам'яті. Вся пам'ять, що зберігає результат, буде автоматично звільнена після завершення сценарію.

### Список параметрів

`statement`

Ідентифікатор результату.

### Значення, що повертаються

Завжди повертає **`true`**

### Примітки

> **Зауваження**
> 
> Якщо автоматична фіксація вимкнена (див. . [odbcautocommit()](function.odbc-autocommit.html)), і **odbcfreeresult()** викликається перед фіксацією, всі транзакції, що очікують, відкочуються.
