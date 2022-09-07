---
navigation:
  - luasandbox.examples.md: « Приклади
  - class.luasandbox.md: LuaSandbox »
  - index.md: PHP Manual
  - luasandbox.examples.md: Приклади
title: Базове використання LuaSandbox
---
## Базове використання LuaSandbox

Після того, як ви скомпілювали PHP з підтримкою LuaSandbox, ви можете почати використовувати LuaSandbox для безпечного виконання наданого користувачем коду Lua.

**Приклад #1 Виконайте код Lua**

```php
<?php

$sandbox = new LuaSandbox;
$sandbox->setMemoryLimit( 50 * 1024 * 1024 );
$sandbox->setCPULimit( 10 );

// Зарегистрируйте некоторые функции в среде Lua

function frobnosticate( $v ) {
    return [ $v + 42 ];
}

$sandbox->registerLibrary( 'php', [
    'frobnosticate' => 'frobnosticate',
    'output' => function ( $string ) {
        echo "$string\n";
    },
    'error' => function () {
        throw new LuaSandboxRuntimeError( "Что-то пошло не так" );
    }
] );

// Выполните некоторый код Lua, включая callback-функции PHP и Lua.

$luaCode = <<<EOF
php.output( "Привет, мир" );

return "Привет", function ( v )
    return php.frobnosticate( v + 200 )
end
EOF;

list( $hi, $frob ) = $sandbox->loadString( $luaCode )->call();
assert( $frob->call( 4000 ) === [ 4242 ] );

// Вызываемые PHP исключения LuaSandboxRuntimeError могут быть пойманы внутри Lua

list( $ok, $message ) = $sandbox->loadString( 'return pcall( php.error )' )->call();
assert( !$ok );
assert( $message === 'Что-то пошло не так' );

?>
```
