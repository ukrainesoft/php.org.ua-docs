---
navigation:
  - luasandbox.loadstring.md: '« LuaSandbox::loadString'
  - luasandbox.registerlibrary.md: 'LuaSandbox::registerLibrary »'
  - index.md: PHP Manual
  - class.luasandbox.md: LuaSandbox
title: 'LuaSandbox::pauseUsageTimer'
---
# LuaSandbox::pauseUsageTimer

(PECL luasandbox >= 1.4.0)

LuaSandbox::pauseUsageTimer — Зупиняє таймер використання процесора

### Опис

```methodsynopsis
public LuaSandbox::pauseUsageTimer(): bool
```

Зупиняє таймер використання процесора.

Має значення тільки за виклику з callback-функції Lua. Коли виконання повертається до Lua, таймер автоматично відновлює роботу. Якщо буде здійснено новий виклик у Lua, таймер буде відновлено під час цього виклику.

Якщо callback-функція PHP знову викликає Lua з не призупиненим таймером, а потім ця функція Lua знову викликає PHP, другий виклик PHP не зможе призупинити таймер. Логіка полягає в тому, що навіть якщо другий виклик PHP не враховує використання процесора відповідно до обмеження, перший виклик все одно його вважає.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає логічне значення (bool), що вказує, чи зупинено таймер.

### Приклади

**Приклад #1 Керування таймером використання**

```php
<?php

// создание нового LuaSandbox и установка лимита процессора
$sandbox = new LuaSandbox();
$sandbox->setCPULimit( 1 );

function doWait( $t ) {
    $end = microtime( true ) + $t;
    while ( microtime( true ) < $end ) {
        // waste CPU cycles
    }
}

// регистрация новой callback-функции PHP
$sandbox->registerLibrary( 'php', [
    'test' => function () use ( $sandbox ) {
        $sandbox->pauseUsageTimer();
        doWait( 5 );

        $sandbox->unpauseUsageTimer();
        doWait( 0.1 );
    },
    'test2' => function () use ( $sandbox ) {
        $sandbox->pauseUsageTimer();
        $sandbox->unpauseUsageTimer();
        doWait( 1.1 );
    }
] );

echo "Это не должно истекать...\n";
$sandbox->loadString( 'php.test()' )->call();

echo "Это должно истекать.\n";
try {
    $sandbox->loadString( 'php.test2()' )->call();
    echo "Это не так?\n";
} catch ( LuaSandboxTimeoutError $ex ) {
    echo "Это так! " . $ex->getMessage() . "\n";
}

?>
```

Результат виконання цього прикладу:

```
Это не должно истекать...
Это должно истекать.
Это так! The maximum execution time for this script was exceeded
```

### Дивіться також

-   [LuaSandbox::setCPULimit()](luasandbox.setcpulimit.md) - Встановлює обмеження часу процесора для середовища Lua
-   [LuaSandbox::unpauseUsageTimer()](luasandbox.unpauseusagetimer.md) - Відновлює таймер, зупинений LuaSandbox::pauseUsageTimer
