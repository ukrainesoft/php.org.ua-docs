Реєструє набір PHP-функцій як бібліотеку Lua

-   [« LuaSandbox::pauseUsageTimer](luasandbox.pauseusagetimer.md)
    
-   [LuaSandbox::setCPULimit »](luasandbox.setcpulimit.md)
    
-   [PHP Manual](index.md)
    
-   [LuaSandbox](class.luasandbox.md)
    
-   Реєструє набір PHP-функцій як бібліотеку Lua
    

# LuaSandbox::registerLibrary

(PECL luasandbox >= 1.0.0)

LuaSandbox::registerLibrary — Реєструє набір PHP-функцій як бібліотеку Lua

### Опис

```methodsynopsis
public LuaSandbox::registerLibrary(string $libname, array $functions): void
```

Реєструє набір PHP-функцій як бібліотеку Lua, щоб Lua міг викликати відповідний PHP-код.

Для отримання додаткової інформації про виклик функцій Lua та значення, що повертаються дивіться [LuaSandboxFunction::call()](luasandboxfunction.call.md)

### Список параметрів

`libname`

Назва бібліотеки. У стані Lua глобальна змінна з цим ім'ям буде встановлено таблицю функцій. Якщо таблиця вже існує, до неї буде додано нові функції.

`functions`

Масив (array), де кожен ключ - це ім'я функції, а кожне значення - це відповідний ([callable](language.types.callable.md)) PHP-код.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Реєстрація PHP-функцій для виклику з Lua**

```php
<?php

// создание нового LuaSandbox
$sandbox = new LuaSandbox();

// регистрация некоторых функций в среде Lua

function frobnosticate( $v ) {
    return [ $v + 42 ];
}

$sandbox->registerLibrary( 'php', [
    'frobnosticate' => 'frobnosticate',
    'output' => function ( $string ) {
        echo "$string\n";
    },
    'error' => function () {
        throw new LuaSandboxRuntimeError( "Что-то пошло не так" );
    }
] );

?>
```

### Дивіться також

-   [LuaSandbox::loadString()](luasandbox.loadstring.md) - Завантажує код Lua у середу Lua
-   [LuaSandbox::wrapPhpFunction()](luasandbox.wrapphpfunction.md) - Обертає викликаний PHP-об'єкт у LuaSandboxFunction