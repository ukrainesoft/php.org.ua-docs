---
navigation:
  - class.luasandbox.md: « LuaSandbox
  - luasandbox.disableprofiler.md: 'LuaSandbox::disableProfiler »'
  - index.md: PHP Manual
  - class.luasandbox.md: LuaSandbox
title: 'LuaSandbox::callFunction'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# LuaSandbox::callFunction

(PECL luasandbox >= 1.0.0)

LuaSandbox::callFunction — Викликає функцію в глобальній змінній Lua

### Опис

```methodsynopsis
public LuaSandbox::callFunction(string $name, mixed ...$args): array|bool
```

Викликає функцію у глобальній змінній Lua.

Якщо ім'я містить символи ".", функція знаходиться через рекурсивний доступ до таблиці, начебто ім'я було виразом Lua.

Якщо змінна не існує або не є функцією, буде повернено false і буде видано попередження.

Для отримання додаткової інформації про виклик функцій Lua та значення, що повертаються дивіться [LuaSandboxFunction::call()](luasandboxfunction.call.md)

### Список параметрів

`name`

Ім'я змінної Lua.

`args`

Аргументи функції.

### Значення, що повертаються

Повертає масив (array) значень, що повертаються функцією Lua, які можуть бути порожніми або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Виклик функції Lua**

```php
<?php

// создание нового LuaSandbox
$sandbox = new LuaSandbox();

// Вызов Lua-функции string.match
$captures = $sandbox->callFunction( 'string.match', $string, $pattern );

?>
```
