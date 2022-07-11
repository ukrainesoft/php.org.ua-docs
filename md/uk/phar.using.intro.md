- [«Використання Phar-архівів](phar.using.md)
- [Використання Phar-архівів: обгортка потоку phar »](phar.using.stream.md)

- [PHP Manual](index.md)
- [Використання Phar-архівів](phar.using.md)
- Використання Phar-архівів: Вступ

## Використання Phar-архівів: Вступ

Концептуально Phar-архіви аналогічні JAR-архівам Java, але враховують
потреби та гнучкість PHP-додатків. Phar-архів використовується для
поширення закінченого PHP-програми або бібліотеки у вигляді одного
файлу. Додаток, що має вигляд Phar-архіву, використовується точно так
ж, як і будь-яке інше PHP-додаток:

php coolapplication.phar

Використання бібліотеки, що має вигляд Phar-архіву, ідентичне
використання будь-якої іншої PHP-бібліотеки:

`<?phpinclude 'coollibrary.phar';?> `

Обертка потоку `phar` є основою модуля phar, для неї
використання докладно написано [тут](phar.using.stream.md). Обгортка
потоку `phar` надає доступ до файлів усередині phar-архіву з
використанням стандартних файлових функцій PHP:
[fopen()](function.fopen.md), [opendir()](function.opendir.md) та
інших, які працюють із звичайними файлами. Обгортка потоку `phar`
підтримує всі операції читання/запису як над файлами, так і над
каталогами.

`<?phpinclude 'phar://coollibrary.phar/internal/file.php';header('Content-type: image/jpeg');// доступ к phar-архівам може здійснюватись по повному шляху до файлів ('phar:///повний/шлях/до/coollibrary.phar/images/wow.jpg');?> `

Клас [Phar](class.phar.md) реалізує розширені можливості з
доступу до файлів та створення phar-архівів. Використання класу Phar
докладно описано [тут](phar.using.object.md).

`<?phptry {    // відкрити існуючий phar-архів    $p = new Phar('coollibrary.phar', 0); // Phar наследует SPL-класс DirectoryIterator    foreach (new RecursiveIteratorIterator($p) as $file) {        // $file является объектом класса PharFileInfo, который наследует SplFileInfo        echo $file->getFileName() . "
";        echo file_get_contents($file->getPathName()) . "
"; // відображує вміст;   }   if (isset($p['internal/file.php'])) {       var_dump($p['internal/file.php']   | новый phar-архив - параметр phar.readonly в php.ini должен быть 0    // phar.readonly включён по умолчанию из соображений безопасности.    // На работающих серверах phar-архивы никогда не должны создаваться,    // а только выполняться.    if (Phar ::canWrite()) {         $p = new Phar('newphar.tar.phar', 0, 'newphar.tar.phar');         /с створити  .gz)        $p = $p->convertToExecutable(Phar::TAR, Phar::GZ);        // создать транзакцию - в newphar.phar ничего не будет записано        // до тех пор, пока не будет вызван stopBuffering(), однако для этого требуется временное хранилище        $p->startBuffering();        // добавить все файлы в каталоге /путь/к/проекту/project, сохранение в phar-архив с префиксом "project"        $p->buildFromIterator(new RecursiveIteratorIterator(new Rec ursiveDirectoryIterator('/шлях/к/проекту/project')), '/шлях/к/проекту/'); // додати новий файл використовуючи ArrayAccess        $p['file1.txt'] = 'Інформація'; $fp = fopen('hugefile.dat', 'rb'); // скопіювати всі дані із потоку        $p['data/hugefile.dat'] = $fp; if (Phar::canCompress(Phar::GZ)) {            $p['data/hugefile.dat']->compress(Phar::GZ); }        $$['images/wow.jpg'] = file_get_contents('images/wow.jpg'); // буде значення може бути збережено в якості метаданих файла        $p['images/wow.jpg']->setMetadata(array('mime-type' => 'image/jpe $p['index.php'] = file_get_contents('index.php'); $p->setMetadata(array('bootstrap' => 'index.php')); // зберегти phar-архів на диск        $p->stopBuffering(); }} catch (Exception $e) {    echo 'Неможливо відкрити Phar: ', $e;}?> `

Крім того, перевірка вмісту phar-файлу може бути здійснена з
допомогою будь-якого з підтримуваних симетричних алгоритмів хешування
(MD5, SHA1, SHA256 і SHA512, якщо ext/hash включений), а також за допомогою
підписування асиметричними відкритим/закритим ключами, використовуючи
OpenSSL. Для того, щоб використовувати підписування OpenSSL, вам
необхідно згенерувати пару з відкритого та закритого ключів та
встановити закритий ключ для підписування, використовуючи
[Phar::setSignatureAlgorithm()](phar.setsignaturealgorithm.md). Крім
того, відкритий ключ, витягнутий за допомогою цього коду:

` <?php$public = openssl_get_publickey(file_get_contents('private.pem'));$pkey = '';openssl_pkey_export($public, $pkey);?> `

повинен бути збережений поруч із phar-архівом, для перевірки якого він
використовується. Якщо phar-архів збережений як
`/шлях/к/моєму/архіву/my.phar`, то відкритий ключ повинен бути збережений
як `/шлях/к/моєму/архіву/my.phar.pubkey`, інакше phar не зможе
перевірити справжність підпису OpenSSL.

Клас [Phar](class.phar.md) також надає 3 статичні методи:
[Phar::webPhar()](phar.webphar.md),
[Phar::mungServer()](phar.mungserver.md) та
[Phar::interceptFileFuncs()](phar.interceptfilefuncs.md), які
мають вирішальне значення для упаковки PHP-додатків, призначених для
використання на звичайних файлових системах та для веб-додатків.
[Phar::webPhar()](phar.webphar.md) реалізує фронтальний контролер,
який спрямовує HTTP-дзвінки у правильне місце всередині phar-архіву.
[Phar::mungServer()](phar.mungserver.md) використовується для зміни
значень масиву `$_SERVER`, що дозволяє обдурити додатки,
обробляють ці значення.
[Phar::interceptFileFuncs()](phar.interceptfilefuncs.md) інструктує
Phar про необхідність перехоплення дзвінків [fopen()](function.fopen.md),
[file_get_contents()](function.file-get-contents.md),
[opendir()](function.opendir.md) та інших функцій, заснованих на stat
([file_exists()](function.file-exists.md),
[is_readable()](function.is-readable.md) і так далі) і
перенаправлення всіх відносних шляхів усередину phar-архіву.

Наприклад, для упаковки випуску популярної програми phpMyAdmin для нього
використання як phar-архів, потрібен тільки цей простий
скрипт, а `phpMyAdmin.phar.tar.php` буде доступний як звичайний файл на
вашому веб-сервері після зміни значень user/password:

` <?php@unlink('phpMyAdmin.phar.tar.php');copy('phpMyAdmin-2.11.3-english.tar.gz', 'phpMyAdmin.phar.tar.php');$a = new Phar ('phpMyAdmin.phar.tar.php');$a->startBuffering();$a["phpMyAdmin-2.11.3-english/config.inc.php"] = '<?php/* Конфігурація сервера *// $i = 0;/* Сервер localhost (config:root) [1] */$i++;$cfg[\'Servers\'][$i][\'host\'] = \'localhost\';$ cfg[\'Servers\'][$i][\'extension\'] = \'mysqli\';$cfg[\'Servers\'][$i][\'connect_type\'] = \'tcp \';$cfg[\'Servers\'][$i][\'compress\'] = false;$cfg[\'Servers\'][$i][\'auth_type\'] = \'config \';$cfg[\'Servers\'][$i][\'user\'] = \'root\';$cfg[\'Servers\'][$i][\'password\'] = \'\';/* Кінець конфігурації сервера */if (strpos(PHP_OS, \'WIN\') !== false) {   $cfg[\'UploadDir\'] = getcwd(                ??? [\'UploadDir\'] = \'/tmp/pharphpmyadmin\'; @mkdir(\'/tmp/pharphpmyadmin\'); @chmod(\'/tmp/pharphpmyadmin\', 0777);}';$a->setStub('<?phpPhar::interceptFileFuncs();Phar::webPhar("phpMyAdmin.phar", "phpMyAdmin-2.11. 3-english/index.php");echo "phpMyAdmin призначений для виконання у веб-браузері
";exit -1;__HALT_COMPILER();');$a->stopBuffering();?> `
