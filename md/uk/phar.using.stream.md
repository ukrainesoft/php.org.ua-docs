---
navigation:
  - phar.using.intro.md: '« Использование Phar-архивов: Введение'
  - phar.using.object.md: 'Використання Phar-архівів: класи Phar та PharData »'
  - index.md: PHP Manual
  - phar.using.md: Использование Phar-архивов
title: 'Використання Phar-архівів: обгортка потоку phar'
---
## Використання Phar-архівів: обгортка потоку phar

Обгортка потоку Phar повністю підтримує [fopen()](function.fopen.md) для читання та запису (не для додавання), [unlink()](function.unlink.md) [stat()](function.stat.md) [fstat()](function.fstat.md) [fseek()](function.fseek.md) [rename()](function.rename.md) та потокові операції каталогів, такі як [opendir()](function.opendir.md) [rmdir()](function.rmdir.md) і [mkdir()](function.mkdir.md)

Також за допомогою контекстів потоку можна впливати на стиснення окремих файлів і метадані пофайлові в Phar-архіві:

```php
<?php
$context = stream_context_create(array('phar' =>
                                    array('compress' => Phar::GZ)),
                                    array('metadata' => array('user' => 'cellog')));
file_put_contents('phar://my.phar/somefile.php', 0, $context);
?>
```

Обгортка потоку `phar` не працює з файлами, розташованими віддалено, і не може з ними працювати, так що її використання можливе навіть коли параметри INI [allowurlfopen](filesystem.configuration.md#ini.allow-url-fopen) і [allowurlinclude](filesystem.configuration.md#ini.allow-url-include) вимкнено.

Незважаючи на наявність можливості створювати phar-архіви з нуля, просто використовуючи потокові операції, найкращим рішенням буде використання функціоналу, вбудованого в клас Phar. Обгортку потоку найкраще використовувати лише читання.
