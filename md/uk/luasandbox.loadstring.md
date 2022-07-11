- [« LuaSandbox::loadBinary](luasandbox.loadbinary.md)
- [LuaSandbox::pauseUsageTimer »](luasandbox.pauseusagetimer.md)

- [PHP Manual](index.md)
- [LuaSandbox](class.luasandbox.md)
- Завантажує код Lua у середу Lua

# LuaSandbox::loadString

(PECL luasandbox \>= 1.0.0)

LuaSandbox::loadString — Завантажує код Lua у середу Lua

### Опис

public **LuaSandbox::loadString**(string `$code`, string `$chunkName` =
''): [LuaSandboxFunction](class.luasandboxfunction.md)

Завантажує код Lua у середу Lua.

Це еквівалент стандартної функції Lua `loadstring()`.

### Список параметрів

`code`
Код Lua.

`chunkName`
Ім'я завантаженого фрагмента для використання у трасуванні помилок.

### Значення, що повертаються

Повертає [LuaSandboxFunction](class.luasandboxfunction.md), який
при виконанні виконає переданий $code.

### Приклади

**Приклад #1 Завантаження коду в Lua**

` <?php// створення нового LuaSandbox$sandbox = new LuaSandbox();// Завантаження кода$function = $sandbox->loadString(<<<CODE     return "Звіт| || $function->call() );?> `

Результат виконання цього прикладу:

array(1) {
[0]=>
string(12) "Привіт, мир!"
}

### Дивіться також

- [LuaSandbox::registerLibrary()](luasandbox.registerlibrary.md) -
Реєструє набір PHP-функцій як бібліотеку Lua
- [LuaSandbox::wrapPhpFunction()](luasandbox.wrapphpfunction.md) -
Обертає викликаний PHP-об'єкт у LuaSandboxFunction
