---
navigation:
  - function.sqlsrv-commit.md: « sqlsrv\_commit
  - function.sqlsrv-connect.md: sqlsrv\_connect »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrv\_configure
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqlsrv\_configure

(No version information available, might only be in Git)

sqlsrv\_configure — Змінює конфігурацію обробки помилок драйвера та ведення журналу

### Опис

```methodsynopsis
sqlsrv_configure(string $setting, mixed $value): bool
```

Змінює конфігурацію обробки помилок драйвера та ведення журналу.

### Список параметрів

`setting`

Ім'я налаштування. Можливі значення: "WarningsReturnAsErrors", "LogSubsystems" та "LogSeverity".

`value`

Значення вказаного параметра. У наступній таблиці показано можливі значення:

**Параметри налаштування помилок та ведення журналу**

| Настройка | Опции |
| --- | --- |
| WarningsReturnAsErrors | 1 (**`true`**) або 0 (**`false`**) . |
| LogSubsystems | SQLSRV\_LOG\_SYSTEM\_ALL (-1) SQLSRV\_LOG\_SYSTEM\_CONN (2) SQLSRV\_LOG\_SYSTEM\_INIT (1) SQLSRV\_LOG\_SYSTEM\_OFF (0) SQLSRV\_LOG\_SYSTEM\_STMT (4) SQLSRV\_LOG\_SYSTEM\_UTIL (8) |
| LogSeverity | SQLSRV\_LOG\_SEVERITY\_ALL (-1) SQLSRV\_LOG\_SEVERITY\_ERROR (1) SQLSRV\_LOG\_SEVERITY\_NOTICE (4) SQLSRV\_LOG\_SEVERITY\_WARNING (2) |

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [» Обробка помилок SQLSRV](http://msdn.microsoft.com/en-us/library/cc626302.aspx)
-   [» Ведення журналу активності SQLSRV](http://msdn.microsoft.com/en-us/library/cc296188.aspx)
