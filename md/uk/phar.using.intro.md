Використання Phar-архівів: Вступ

-   [« Использование Phar-архивов](phar.using.html)
    
-   [Использование Phar-архивов: обёртка потока phar »](phar.using.stream.html)
    
-   [PHP Manual](index.html)
    
-   [Использование Phar-архивов](phar.using.html)
    
-   Використання Phar-архівів: Вступ
    

## Використання Phar-архівів: Вступ

Концептуально Phar-архіви аналогічні JAR-архівам Java, але враховують потреби та гнучкість PHP-додатків. Phar-архів використовується для поширення закінченого PHP-програми або бібліотеки у вигляді одного файлу. Додаток, що має вигляд Phar-архіву, використовується в точності так само, як і будь-який інший PHP-додаток:

```
php coolapplication.phar
```

Використання бібліотеки, що має вигляд Phar-архіву, ідентичне використанню будь-якої іншої PHP-бібліотеки:

```php
<?php
include 'coollibrary.phar';
?>
```

Обгортка потоку `phar` є основою модуля phar, для її використання докладно написано [здесь](phar.using.stream.html). Обгортка потоку `phar` надає доступ до файлів усередині phar-архіву з використанням стандартних файлових функцій PHP: [fopen()](function.fopen.html) [opendir()](function.opendir.html) та інших, які працюють із звичайними файлами. Обгортка потоку `phar` підтримує всі операції читання/запису як над файлами, і над каталогами.

```php
<?php
include 'phar://coollibrary.phar/internal/file.php';
header('Content-type: image/jpeg');
// доступ к phar-архивам может осуществляться по полному пути или с помощью псевдонима
echo file_get_contents('phar:///полный/путь/к/coollibrary.phar/images/wow.jpg');
?>
```

Клас [Phar](class.phar.html) реалізує розширені можливості доступу до файлів і створення phar-архівів. Використання класу Phar докладно описано [здесь](phar.using.object.html)

```php
<?php
try {
    // открыть существующий phar-архив
    $p = new Phar('coollibrary.phar', 0);
    // Phar наследует SPL-класс DirectoryIterator
    foreach (new RecursiveIteratorIterator($p) as $file) {
        // $file является объектом класса PharFileInfo, который наследует SplFileInfo
        echo $file->getFileName() . "\n";
        echo file_get_contents($file->getPathName()) . "\n"; // отображает содержимое;
    }
    if (isset($p['internal/file.php'])) {
        var_dump($p['internal/file.php']->getMetadata());
    }

    // создать новый phar-архив - параметр phar.readonly в php.ini должен быть 0
    // phar.readonly включён по умолчанию из соображений безопасности.
    // На работающих серверах phar-архивы никогда не должны создаваться,
    // а только выполняться.
    if (Phar::canWrite()) {
        $p = new Phar('newphar.tar.phar', 0, 'newphar.tar.phar');
        // создать phar-архив, основанный на tar, сжатый gzip-сжатием (.tar.gz)
        $p = $p->convertToExecutable(Phar::TAR, Phar::GZ);

        // создать транзакцию - в newphar.phar ничего не будет записано
        // до тех пор, пока не будет вызван stopBuffering(), однако для этого требуется временное хранилище
        $p->startBuffering();
        // добавить все файлы в каталоге /путь/к/проекту/project, сохранение в phar-архив с префиксом "project"
        $p->buildFromIterator(new RecursiveIteratorIterator(new RecursiveDirectoryIterator('/путь/к/проекту/project')), '/путь/к/проекту/');

        // добавить новый файл используя ArrayAccess
        $p['file1.txt'] = 'Информация';
        $fp = fopen('hugefile.dat', 'rb');
        // скопировать все данные из потока
        $p['data/hugefile.dat'] = $fp;

        if (Phar::canCompress(Phar::GZ)) {
            $p['data/hugefile.dat']->compress(Phar::GZ);
        }

        $p['images/wow.jpg'] = file_get_contents('images/wow.jpg');
        // любое значение может быть сохранено в качестве метаданных файла
        $p['images/wow.jpg']->setMetadata(array('mime-type' => 'image/jpeg'));
        $p['index.php'] = file_get_contents('index.php');
        $p->setMetadata(array('bootstrap' => 'index.php'));

        // сохранить phar-архив на диск
        $p->stopBuffering();
    }
} catch (Exception $e) {
    echo 'Невозможно открыть Phar: ', $e;
}
?>
```

Крім того, перевірка вмісту phar-файлу може бути здійснена за допомогою будь-якого з підтримуваних симетричних алгоритмів хешування (MD5, SHA1, SHA256 та SHA512, якщо ext/hash включений), а також за допомогою підписування асиметричними відкритим/закритим ключами, використовуючи OpenSSL. Для того щоб використовувати підписування OpenSSL, вам необхідно згенерувати пару з відкритого та закритого ключів та встановити закритий ключ для підписування, використовуючи [Phar::setSignatureAlgorithm()](phar.setsignaturealgorithm.html). Крім того, відкритий ключ, витягнутий за допомогою цього коду:

```php
<?php
$public = openssl_get_publickey(file_get_contents('private.pem'));
$pkey = '';
openssl_pkey_export($public, $pkey);
?>
```

повинен бути збережений поруч із phar-архівом, для перевірки якого він використовується. Якщо phar-архів збережений як `/путь/к/моему/архиву/my.phar`, то відкритий ключ повинен бути збережений як `/путь/к/моему/архиву/my.phar.pubkey`, інакше phar не зможе перевірити справжність підпису OpenSSL.

Клас [Phar](class.phar.html) також надає 3 статичні методи: [Phar::webPhar()](phar.webphar.html) [Phar::mungServer()](phar.mungserver.html) і [Phar::interceptFileFuncs()](phar.interceptfilefuncs.html), які мають вирішальне значення для упаковки PHP-додатків, призначених для використання на звичайних файлових системах та для веб-додатків . [Phar::webPhar()](phar.webphar.html) реалізує фронтальний контролер, який направляє HTTP-дзвінки у правильне місце всередині phar-архіву . [Phar::mungServer()](phar.mungserver.html) використовується для зміни значень масиву [$\_SERVER](reserved.variables.server.html)що дозволяє обдурити додатки, що обробляють ці значення . [Phar::interceptFileFuncs()](phar.interceptfilefuncs.html) інструктує Phar про необхідність перехоплення дзвінків [fopen()](function.fopen.html) [file\_get\_contents()](function.file-get-contents.html) [opendir()](function.opendir.html) та інших функцій, заснованих на stat ([file\_exists()](function.file-exists.html) [is\_readable()](function.is-readable.html) і так далі) і перенаправлення всіх відносних шляхів усередину phar-архіву.

Наприклад, для упаковки випуску популярної програми phpMyAdmin для його використання як phar-архів, потрібен тільки цей простий скрипт, а `phpMyAdmin.phar.tar.php` буде доступний як звичайний файл на вашому веб-сервері після зміни значень user/password:

```php
<?php
@unlink('phpMyAdmin.phar.tar.php');
copy('phpMyAdmin-2.11.3-english.tar.gz', 'phpMyAdmin.phar.tar.php');
$a = new Phar('phpMyAdmin.phar.tar.php');
$a->startBuffering();
$a["phpMyAdmin-2.11.3-english/config.inc.php"] = '<?php
/* Конфигурация сервера */
$i = 0;

/* Сервер localhost (config:root) [1] */
$i++;
$cfg[\'Servers\'][$i][\'host\'] = \'localhost\';
$cfg[\'Servers\'][$i][\'extension\'] = \'mysqli\';
$cfg[\'Servers\'][$i][\'connect_type\'] = \'tcp\';
$cfg[\'Servers\'][$i][\'compress\'] = false;
$cfg[\'Servers\'][$i][\'auth_type\'] = \'config\';
$cfg[\'Servers\'][$i][\'user\'] = \'root\';
$cfg[\'Servers\'][$i][\'password\'] = \'\';


/* Конец конфигурации сервера */
if (strpos(PHP_OS, \'WIN\') !== false) {
    $cfg[\'UploadDir\'] = getcwd();
} else {
    $cfg[\'UploadDir\'] = \'/tmp/pharphpmyadmin\';
    @mkdir(\'/tmp/pharphpmyadmin\');
    @chmod(\'/tmp/pharphpmyadmin\', 0777);
}';
$a->setStub('<?php
Phar::interceptFileFuncs();
Phar::webPhar("phpMyAdmin.phar", "phpMyAdmin-2.11.3-english/index.php");
echo "phpMyAdmin предназначен для выполнения в веб-браузере\n";
exit -1;
__HALT_COMPILER();
');
$a->stopBuffering();
?>
```