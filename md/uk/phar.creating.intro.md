Створення Phar-архівів: Вступ

-   [« Создание Phar-архивов](phar.creating.html)
    
-   [Чим відрізняється phar від tar-або zip-архіву? »](phar.fileformat.html)
    
-   [PHP Manual](index.html)
    
-   [Создание Phar-архивов](phar.creating.html)
    
-   Створення Phar-архівів: Вступ
    

## Створення Phar-архівів: Вступ

Має бути написано в найближчому майбутньому. Перед читанням цього обов'язково прочитайте [Як використовувати Phar-архіви](phar.using.html)

Відмінним початком буде читання про [Phar::buildFromIterator()](phar.buildfromiterator.html) та про особливості вибору доступного для архівів [формата файла](phar.fileformat.html). Хороше розуміння того, що являє собою заглушка (stub) і що вона має вирішальне значення для створення phar-архіву, і тому [Phar::setStub()](phar.setstub.html) і [Phar::createDefaultStub()](phar.createdefaultstub.html) також будуть гарною відправкою точкою. Якщо ви розповсюджуєте веб-додаток, ключовими будуть знання про [Phar::webPhar()](phar.webphar.html) та пов'язаному з ним методі [Phar::mungServer()](phar.mungserver.html). Будь-яка програма, яка звертається до своїх власних файлів, повинна враховувати можливість використання [Phar::interceptFileFuncs()](phar.interceptfilefuncs.html)