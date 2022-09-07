---
navigation:
  - phar.creating.md: « Создание Phar-архивов
  - phar.fileformat.md: Чим відрізняється phar від tar-або zip-архіву? »
  - index.md: PHP Manual
  - phar.creating.md: Создание Phar-архивов
title: 'Створення Phar-архівів: Вступ'
---
## Створення Phar-архівів: Вступ

Має бути написано в найближчому майбутньому. Перед читанням цього обов'язково прочитайте [Як використовувати Phar-архіви](phar.using.md)

Відмінним початком буде читання про [Phar::buildFromIterator()](phar.buildfromiterator.md) та про особливості вибору доступного для архівів [формата файла](phar.fileformat.md). Хороше розуміння того, що являє собою заглушка (stub) і що вона має вирішальне значення для створення phar-архіву, і тому [Phar::setStub()](phar.setstub.md) і [Phar::createDefaultStub()](phar.createdefaultstub.md) також будуть гарною відправкою точкою. Якщо ви розповсюджуєте веб-додаток, ключовими будуть знання про [Phar::webPhar()](phar.webphar.md) та пов'язаному з ним методі [Phar::mungServer()](phar.mungserver.md). Будь-яка програма, яка звертається до своїх власних файлів, повинна враховувати можливість використання [Phar::interceptFileFuncs()](phar.interceptfilefuncs.md)
