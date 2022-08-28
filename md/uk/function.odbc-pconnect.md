Відкриває постійне з'єднання з базою даних

-   [« odbc\_num\_rows](function.odbc-num-rows.html)
    
-   [odbc\_prepare »](function.odbc-prepare.html)
    
-   [PHP Manual](index.html)
    
-   [Функции ODBC](ref.uodbc.html)
    
-   Відкриває постійне з'єднання з базою даних
    

# odbcpconnect

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcpconnect — Відкриває постійне з'єднання з базою даних

### Опис

```methodsynopsis
odbc_pconnect(    string $dsn,    string $user,    string $password,    int $cursor_option = SQL_CUR_USE_DRIVER): resource|false
```

Відкриває постійне з'єднання з базою даних.

Функція дуже схожа на [odbc\_connect()](function.odbc-connect.html), крім того, що з'єднання насправді не закривається після завершення роботи скрипта. Наступні запити на з'єднання з тією самою комбінацією `dsn` `user` і `password` (за допомогою [odbc\_connect()](function.odbc-connect.html) і **odbcpconnect()**) можуть повторно використовувати постійне з'єднання.

### Список параметрів

Для більш детальної інформації варто звернутись до опису [odbc\_connect()](function.odbc-connect.html)

### Значення, що повертаються

Повертає з'єднання ODBC або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**: Постійні з'єднання не діють, якщо PHP використовується як CGI.

### Дивіться також

-   [odbc\_connect()](function.odbc-connect.html) - З'єднує із джерелом даних
-   [Постоянные соединения с базами данных](features.persistent-connections.html)