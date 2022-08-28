Журналування налагоджувальної інформації

-   [« mysqli::debug](mysqli.debug.html)
    
-   [mysqli::$errno »](mysqli.errno.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Журналування налагоджувальної інформації
    

# mysqli::dumpdebuginfo

# mysqlidumpdebuginfo

(PHP 5, PHP 7, PHP 8)

mysqli::dumpdebuginfo -- mysqlidumpdebuginfo — Журналування налагоджувальної інформації

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::dump_debug_info(): bool
```

Процедурний стиль

```methodsynopsis
mysqli_dump_debug_info(mysqli $mysql): bool
```

Функція розроблена для запуску від імені користувача з привілеями SUPER і використовується для складання налагоджувальної інформації в журнал сервера MySQL, до якого здійснено підключення.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqli\_connect()](function.mysqli-connect.html) або [mysqli\_init()](mysqli.init.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [mysqli\_debug()](mysqli.debug.html) - Виконує процедури налагодження