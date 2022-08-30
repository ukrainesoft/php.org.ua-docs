Використання Phar-архівів: обгортка потоку phar

-   [« Использование Phar-архивов: Введение](phar.using.intro.html)
    
-   [Використання Phar-архівів: класи Phar та PharData »](phar.using.object.html)
    
-   [PHP Manual](index.html)
    
-   [Использование Phar-архивов](phar.using.html)
    
-   Використання Phar-архівів: обгортка потоку phar
    

## Використання Phar-архівів: обгортка потоку phar

Обгортка потоку Phar повністю підтримує [fopen()](function.fopen.html) для читання та запису (не для додавання), [unlink()](function.unlink.html) [stat()](function.stat.html) [fstat()](function.fstat.html) [fseek()](function.fseek.html) [rename()](function.rename.html) та потокові операції каталогів, такі як [opendir()](function.opendir.html) [rmdir()](function.rmdir.html) і [mkdir()](function.mkdir.html)

Також за допомогою контекстів потоку можна впливати на стиснення окремих файлів і метадані пофайлові в Phar-архіві:

```php
<?php
$context = stream_context_create(array('phar' =>
                                    array('compress' => Phar::GZ)),
                                    array('metadata' => array('user' => 'cellog')));
file_put_contents('phar://my.phar/somefile.php', 0, $context);
?>
```

Обгортка потоку `phar` не працює з файлами, розташованими віддалено, і не може з ними працювати, так що її використання можливе навіть коли параметри INI [allowurlfopen](filesystem.configuration.html#ini.allow-url-fopen) і [allowurlinclude](filesystem.configuration.html#ini.allow-url-include) вимкнено.

Незважаючи на наявність можливості створювати phar-архіви з нуля, просто використовуючи потокові операції, найкращим рішенням буде використання функціоналу, вбудованого в клас Phar. Обгортку потоку найкраще використовувати лише читання.