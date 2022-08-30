Ініціалізує запит і повертає об'єкт для використання в mysqlistmtprepare

-   [« mysqli::stat](mysqli.stat.html)
    
-   [mysqli::storeresult »](mysqli.store-result.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Ініціалізує запит і повертає об'єкт для використання в mysqlistmtprepare
    

# mysqli::stmtinit

# mysqlistmtinit

(PHP 5, PHP 7, PHP 8)

mysqli::stmtinit - mysqlistmtinit — Ініціалізує запит та повертає об'єкт для використання у mysqlistmtprepare

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::stmt_init(): mysqli_stmt|false
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_init(mysqli $mysql): mysqli_stmt|false
```

Виділяє пам'ять та ініціалізує об'єкт запиту, який можна використовувати у функції [mysqlistmtprepare()](mysqli-stmt.prepare.html)

> **Зауваження**
> 
> Усі наступні виклики mysqlistmt функцій викликають помилку, доки не буде викликана функція [mysqlistmtprepare()](mysqli-stmt.prepare.html)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.html)

### Значення, що повертаються

Повертає об'єкт.

### Дивіться також

-   [mysqlistmtprepare()](mysqli-stmt.prepare.html) - готує затвердження SQL до виконання