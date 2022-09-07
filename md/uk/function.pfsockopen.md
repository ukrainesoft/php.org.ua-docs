---
navigation:
  - function.openlog.md: « openlog
  - function.setcookie.md: setcookie »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: pfsockopen
---
# pfsockopen

(PHP 4, PHP 5, PHP 7, PHP 8)

pfsockopen — Відкриває постійне з'єднання з інтернет-сокетом або доменним сокетом Unix

### Опис

```methodsynopsis
pfsockopen(    string $hostname,    int $port = -1,    int &$error_code = null,    string &$error_message = null,    ?float $timeout = null): resource|false
```

Ця функція є повним аналогом функції [fsockopen()](function.fsockopen.md) з тією різницею, що з'єднання не закривається після завершення роботи скрипта. Це версія функції [fsockopen()](function.fsockopen.md) із можливістю постійного підключення.

### Список параметрів

Для отримання інформації про параметр дивіться документацію по [fsockopen()](function.fsockopen.md)

### Значення, що повертаються

**pfsockopen()** повертає файловий покажчик, який можна використовувати з функціями, що працюють із файлами (такі як [fgets()](function.fgets.md) [fgetss()](function.fgetss.md) [fwrite()](function.fwrite.md) [fclose()](function.fclose.md) і [feof()](function.feof.md)) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `timeout` тепер допускає значення null. |

### Дивіться також

-   [fsockopen()](function.fsockopen.md) - Відкриває з'єднання з інтернет-сокетом або доменним сокетом Unix
