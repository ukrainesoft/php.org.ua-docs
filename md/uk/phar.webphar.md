Надсилає запит із браузера у внутрішній файл у phar-архіві

-   [« Phar::unlinkArchive](phar.unlinkarchive.md)
    
-   [PharData »](class.phardata.md)
    
-   [PHP Manual](index.md)
    
-   [Phar](class.phar.md)
    
-   Надсилає запит із браузера у внутрішній файл у phar-архіві
    

# Phar::webPhar

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::webPhar — Надсилає запит із браузера у внутрішній файл у phar-архіві

### Опис

```methodsynopsis
final public static Phar::webPhar(    ?string $alias = null,    ?string $index = null,    ?string $fileNotFoundScript = null,    array $mimeTypes = [],    ?callable $rewrite = null): void
```

**Phar::webPhar()** служить [Phar::mapPhar()](phar.mapphar.md) для веб-архівів phar. Метод аналізує [SERVER\['REQUESTURI'\]](reserved.variables.server.md) і надсилає запит із браузера у внутрішній файл у phar-архіві. Він імітує веб-сервер, надсилає запити до потрібного файлу, відображає правильні заголовки та аналізує файли PHP у міру потреби. У поєднанні з [Phar::mungServer()](phar.mungserver.md) і [Phar::interceptFileFuncs()](phar.interceptfilefuncs.md), будь-який веб-додаток можна використовувати без змін із phar-архіву.

**Phar::webPhar()** повинен викликатись тільки із заглушки (stub) phar-архіву (про те, що таке заглушка і як з ним працювати, читайте [тут](phar.fileformat.stub.md)

### Список параметрів

`alias`

Псевдонім для використання в обгортках `phar://`

`index`

Розташування в phar-архіві індексного файлу.

`fileNotFoundScript`

Розташування скрипта, який відповідає за обробку помилки HTTP 404. Скрипт повинен повертати коректні заголовки для цієї помилки.

`mimeTypes`

Масив зіставлення розширень файлів типу MIME. Якщо достатньо порівняння за умовчанням, передайте сюди порожній масив. За замовчуванням використовуються такі зіставлення:

```php
<?php
$mimes = array(
    'phps' => Phar::PHPS, // передаётся в highlight_file()
    'c' => 'text/plain',
    'cc' => 'text/plain',
    'cpp' => 'text/plain',
    'c++' => 'text/plain',
    'dtd' => 'text/plain',
    'h' => 'text/plain',
    'log' => 'text/plain',
    'rng' => 'text/plain',
    'txt' => 'text/plain',
    'xsd' => 'text/plain',
    'php' => Phar::PHP, // разбирается как PHP
    'inc' => Phar::PHP, // разбирается как PHP
    'avi' => 'video/avi',
    'bmp' => 'image/bmp',
    'css' => 'text/css',
    'gif' => 'image/gif',
    'htm' => 'text/html',
    'html' => 'text/html',
    'htmls' => 'text/html',
    'ico' => 'image/x-ico',
    'jpe' => 'image/jpeg',
    'jpg' => 'image/jpeg',
    'jpeg' => 'image/jpeg',
    'js' => 'application/x-javascript',
    'midi' => 'audio/midi',
    'mid' => 'audio/midi',
    'mod' => 'audio/mod',
    'mov' => 'movie/quicktime',
    'mp3' => 'audio/mp3',
    'mpg' => 'video/mpeg',
    'mpeg' => 'video/mpeg',
    'pdf' => 'application/pdf',
    'png' => 'image/png',
    'swf' => 'application/shockwave-flash',
    'tif' => 'image/tiff',
    'tiff' => 'image/tiff',
    'wav' => 'audio/wav',
    'xbm' => 'image/xbm',
    'xml' => 'text/xml',
);
?>
```

`rewrite`

Функція перезапису, якою передається єдиний рядковий параметр і яка повинна також повернути рядок, або **`false`**

Якщо ви використовуєте fast-cgi або cgi, то параметром, що передається в цю функцію, буде значення змінної [SERVER\['PATHINFO'\]](reserved.variables.server.md). В іншому випадку буде передаватися значення змінної [SERVER\['REQUESTURI'\]](reserved.variables.server.md)

Якщо буде повернутий рядок, то він буде використаний як шлях до файлу всередині архіву. Якщо повернеться **`false`**, то webPhar() надішле код помилки HTTP 403.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викине виняток [PharException](class.pharexception.md), якщо неможливо відкрити будь-який файл, або викликати її із заглушки. Якщо у параметрі `mimeTypes` вказати некоректний MIME-тип, або `rewrite` буде передана некоректна функція зворотного виклику, то буде викинуто виняток [UnexpectedValueException](class.unexpectedvalueexception.md)

### список змін

| Версия | Описание                                                                     |
|--------|------------------------------------------------------------------------------|
|        | `fileNotFoundScript` `mimeTypes` і `rewrite` тепер допускають значення null. |

### Приклади

**Приклад #1 Приклад використання **Phar::webPhar()****

У прикладі нижче створений phar відобразить `Hello World` при зверненні з браузера до `/myphar.phar/index.php` або до `/myphar.phar`, і відобразить вихідний код `index.phps` при зверненні до `/myphar.phar/index.phps`

```php
<?php
// создаём архив:
try {
    $phar = new Phar('myphar.phar');
    $phar['index.php'] = '<?php echo "Hello World"; ?>';
    $phar['index.phps'] = '<?php echo "Hello World"; ?>';
    $phar->setStub('<?php
Phar::webPhar();
__HALT_COMPILER(); ?>');
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

### Дивіться також

-   [Phar::mungServer()](phar.mungserver.md) - Визначити список до чотирьох $SERVER-змінних, які мають бути змінені для запуску
-   [Phar::interceptFileFuncs()](phar.interceptfilefuncs.md) - Вказує phar перехоплювати fopen, filegetcontents, opendir та всі stat-функції