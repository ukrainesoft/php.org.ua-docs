Встановлює межу пам'яті для середовища Lua

-   [« LuaSandbox::setCPULimit](luasandbox.setcpulimit.html)
    
-   [LuaSandbox::unpauseUsageTimer »](luasandbox.unpauseusagetimer.html)
    
-   [PHP Manual](index.html)
    
-   [LuaSandbox](class.luasandbox.html)
    
-   Встановлює межу пам'яті для середовища Lua
    

# LuaSandbox::setMemoryLimit

(PECL luasandbox >= 1.0.0)

LuaSandbox::setMemoryLimit — Встановлює межу пам'яті для середовища Lua

### Опис

```methodsynopsis
public LuaSandbox::setMemoryLimit(int $limit): void
```

Встановлює межу пам'яті для середовища Lua.

Якщо межа перевищена, буде викинуто виняток [LuaSandboxMemoryError](class.luasandboxmemoryerror.html)

### Список параметрів

`limit`

Межа пам'яті у байтах.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Виклик функції Lua**

```php
<?php

// Создание нового объекта LuaSandbox
$sandbox = new LuaSandbox();

// Установка предела памяти
$sandbox->setMemoryLimit( 50 * 1024 * 1024 );

// Запуск кода Lua
$sandbox->loadString( 'local x = "x"; while true do x = x .. x; end' )->call();

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
PHP Fatal error:  Uncaught LuaSandboxMemoryError: not enough memory
```

### Дивіться також

-   [LuaSandbox::getMemoryUsage()](luasandbox.getmemoryusage.html) - Повертає поточне використання пам'яті у середовищі Lua
-   [LuaSandbox::getPeakMemoryUsage()](luasandbox.getpeakmemoryusage.html) - Повертає пікове використання пам'яті в середовищі Lua
-   [LuaSandbox::setCPULimit()](luasandbox.setcpulimit.html) - Встановлює обмеження часу процесора для середовища Lua