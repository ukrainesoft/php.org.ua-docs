Змінює конфігурацію обробки помилок драйвера та ведення журналу

-   [« sqlsrvcommit](function.sqlsrv-commit.html)
    
-   [sqlsrvconnect »](function.sqlsrv-connect.html)
    
-   [PHP Manual](index.md)
    
-   [Функції SQLSRV](ref.sqlsrv.md)
    
-   Змінює конфігурацію обробки помилок драйвера та ведення журналу
    

# sqlsrvconfigure

(No version information available, might only be in Git)

sqlsrvconfigure — Змінює конфігурацію обробки помилок драйвера та ведення журналу

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
| WarningsReturnAsErrors | **`true`**) або 0 (**`false`** |
| LogSubsystems | SQLSRVLOGSYSTEMALL (-1) SQLSRVLOGSYSTEMCONN (2) SQLSRVLOGSYSTEMINIT (1) SQLSRVLOGSYSTEMOFF (0) SQLSRVLOGSYSTEMSTMT (4) SQLSRVLOGSYSTEMUTIL (8) |
| LogSeverity | SQLSRVLOGSEVERITYALL (-1) SQLSRVLOGSEVERITYERROR (1) SQLSRVLOGSEVERITYNOTICE (4) SQLSRVLOGSEVERITYWARNING (2) |

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [» Обработка ошибок SQLSRV](http://msdn.microsoft.com/en-us/library/cc626302.aspx)
-   [» Ведення журналу активності SQLSRV](http://msdn.microsoft.com/en-us/library/cc296188.aspx)