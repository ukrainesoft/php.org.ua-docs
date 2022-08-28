Відкриває постійне з'єднання з інтернет-сокетом або доменним сокетом Unix

-   [« openlog](function.openlog.html)
    
-   [setcookie »](function.setcookie.html)
    
-   [PHP Manual](index.html)
    
-   [Сетевые функции](ref.network.html)
    
-   Відкриває постійне з'єднання з інтернет-сокетом або доменним сокетом Unix
    

# pfsockopen

(PHP 4, PHP 5, PHP 7, PHP 8)

pfsockopen — Відкриває постійне з'єднання з інтернет-сокетом або доменним сокетом Unix

### Опис

```methodsynopsis
pfsockopen(    string $hostname,    int $port = -1,    int &$error_code = null,    string &$error_message = null,    ?float $timeout = null): resource|false
```

Ця функція є повним аналогом функції [fsockopen()](function.fsockopen.html) з тією різницею, що з'єднання не закривається після завершення роботи скрипта. Це версія функції [fsockopen()](function.fsockopen.html) із можливістю постійного підключення.

### Список параметрів

Для отримання інформації про параметр дивіться документацію по [fsockopen()](function.fsockopen.html)

### Значення, що повертаються

**pfsockopen()** повертає файловий покажчик, який можна використовувати з функціями, що працюють із файлами (такі як [fgets()](function.fgets.html) [fgetss()](function.fgetss.html) [fwrite()](function.fwrite.html) [fclose()](function.fclose.html) і [feof()](function.feof.html)) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `timeout` тепер допускає значення null. |

### Дивіться також

-   [fsockopen()](function.fsockopen.html) - Відкриває з'єднання з інтернет-сокетом або доменним сокетом Unix