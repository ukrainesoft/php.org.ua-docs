- [« Приклади](luasandbox.examples.md)
- [LuaSandbox »](class.luasandbox.md)

- [PHP Manual](index.md)
- [Приклади](luasandbox.examples.md)
- Базове використання LuaSandbox

## Базове використання LuaSandbox

Після того, як ви скомпілювали PHP із підтримкою LuaSandbox, ви можете
почати використовувати LuaSandbox для безпечного виконання
наданого користувачем коду Lua.

**Приклад #1 Виконайте код Lua**

` <?php$sandbox = new LuaSandbox;$sandbox->setMemoryLimit( 50 * 1024 * 1024 );$sandbox->setCPULimit( 10 );// Зарегистрируйте некоторые функции в среде Luafunction frobnosticate( $v ) {    return [ $v + 42 ];}$sandbox->registerLibrary( 'php', [    'frobnosticate' => 'frobnosticate',   'output' => function ( $string ) |
";    },    'error' => function () {        throw new LuaSandboxRuntimeError( "Что-то пошло не так" );    }] );// Выполните некоторый код Lua, включая callback-функции PHP и Lua.$luaCode = < <<EOFphp.output( "Привіт, світ" );return "Привіт", function ( v )   return php.frobnosticate( v + 200 )endEOF;list( $hi, $ )->call();assert( $frob->call( 4000 ) === [ 4242 ] );// Викликаються PHP виключення LuaSandboxRuntimeError можуть бути впіймані s$      'return pcall( php.error )' )->call();assert( !$ok );assert( $message === 'Щось пішло не так' );?> `
