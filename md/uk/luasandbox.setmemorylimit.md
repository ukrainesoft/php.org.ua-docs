---
navigation:
  - luasandbox.setcpulimit.md: '« LuaSandbox::setCPULimit'
  - luasandbox.unpauseusagetimer.md: 'LuaSandbox::unpauseUsageTimer »'
  - index.md: PHP Manual
  - class.luasandbox.md: LuaSandbox
title: 'LuaSandbox::setMemoryLimit'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# LuaSandbox::setMemoryLimit

(PECL luasandbox >= 1.0.0)

LuaSandbox::setMemoryLimit — Встановлює межу пам'яті для середовища Lua

### Опис

```methodsynopsis
public LuaSandbox::setMemoryLimit(int $limit): void
```

Встановлює межу пам'яті для середовища Lua.

Якщо межа перевищена, буде викинуто виняток [LuaSandboxMemoryError](class.luasandboxmemoryerror.md)

### Список параметрів

`limit`

Межа пам'яті в байтах.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Виклик функції Lua**

```php
<?php

// Создание нового объекта LuaSandbox
$sandbox = new LuaSandbox();

// Установка предела памяти
$sandbox->setMemoryLimit( 50 * 1024 * 1024 );

// Запуск кода Lua
$sandbox->loadString( 'local x = "x"; while true do x = x .. x; end' )->call();

?>
```

Висновок наведеного прикладу буде схожим на:

```
PHP Fatal error:  Uncaught LuaSandboxMemoryError: not enough memory
```

### Дивіться також

-   [LuaSandbox::getMemoryUsage()](luasandbox.getmemoryusage.md) \- Повертає поточне використання пам'яті у середовищі Lua
-   [LuaSandbox::getPeakMemoryUsage()](luasandbox.getpeakmemoryusage.md) \- Повертає пікове використання пам'яті в середовищі Lua
-   [LuaSandbox::setCPULimit()](luasandbox.setcpulimit.md) \- Встановлює обмеження часу процесора для середовища Lua
