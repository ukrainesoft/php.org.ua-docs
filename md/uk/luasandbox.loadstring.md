---
navigation:
  - luasandbox.loadbinary.md: '« LuaSandbox::loadBinary'
  - luasandbox.pauseusagetimer.md: 'LuaSandbox::pauseUsageTimer »'
  - index.md: PHP Manual
  - class.luasandbox.md: LuaSandbox
title: 'LuaSandbox::loadString'
---
# LuaSandbox::loadString

(PECL luasandbox >= 1.0.0)

LuaSandbox::loadString — Завантажує код Lua у середу Lua

### Опис

```methodsynopsis
public LuaSandbox::loadString(string $code, string $chunkName = ''): LuaSandboxFunction
```

Завантажує код Lua у середу Lua.

Це еквівалент стандартної функції Lua `loadstring()`

### Список параметрів

`code`

Код Lua.

`chunkName`

Ім'я завантаженого фрагмента для використання у трасуванні помилок.

### Значення, що повертаються

Повертає [LuaSandboxFunction](class.luasandboxfunction.md), який під час виконання виконає переданий $code.

### Приклади

**Приклад #1 Завантаження коду Lua**

```php
<?php

// создание нового LuaSandbox
$sandbox = new LuaSandbox();

// Загрузка кода
$function = $sandbox->loadString(
<<<CODE
    return "Привет, мир!"
CODE
);

// Выполнение загруженного кода
var_dump( $function->call() );

?>
```

Результат виконання цього прикладу:

```
array(1) {
  [0]=>
  string(12) "Привет, мир!"
}
```

### Дивіться також

-   [LuaSandbox::registerLibrary()](luasandbox.registerlibrary.md) - Реєструє набір PHP-функцій як бібліотеку Lua
-   [LuaSandbox::wrapPhpFunction()](luasandbox.wrapphpfunction.md) - Обертає викликаний PHP-об'єкт у LuaSandboxFunction
