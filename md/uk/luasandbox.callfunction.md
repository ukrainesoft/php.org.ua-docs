Викликає функцію у глобальній змінній Lua

-   [« LuaSandbox](class.luasandbox.html)
    
-   [LuaSandbox::disableProfiler »](luasandbox.disableprofiler.html)
    
-   [PHP Manual](index.html)
    
-   [LuaSandbox](class.luasandbox.html)
    
-   Викликає функцію у глобальній змінній Lua
    

# LuaSandbox::callFunction

(PECL luasandbox >= 1.0.0)

LuaSandbox::callFunction — Викликає функцію в глобальній змінній Lua

### Опис

```methodsynopsis
public LuaSandbox::callFunction(string $name, mixed ...$args): array|bool
```

Викликає функцію у глобальній змінній Lua.

Якщо ім'я містить символи ".", функція перебуває через рекурсивний доступ до таблиці, ніби ім'я було виразом Lua.

Якщо змінна не існує або не є функцією, буде повернено false і буде видано попередження.

Для отримання додаткової інформації про виклик функцій Lua та значення, що повертаються дивіться [LuaSandboxFunction::call()](luasandboxfunction.call.html)

### Список параметрів

`name`

Ім'я змінної Lua.

`args`

Аргументи функції.

### Значення, що повертаються

Повертає масив (array) значень, що повертаються функцією Lua, які можуть бути порожніми або `false` у разі виникнення помилки.

### Приклади

**Приклад #1 Виклик функції Lua**

```php
<?php

// создание нового LuaSandbox
$sandbox = new LuaSandbox();

// Вызов Lua-функции string.match
$captures = $sandbox->callFunction( 'string.match', $string, $pattern );

?>
```