---
navigation:
  - phar.creating.md: « Створення Phar-архівів
  - phar.fileformat.md: Чим відрізняється phar від tar-або zip-архіву? »
  - index.md: PHP Manual
  - phar.creating.md: Створення Phar-архівів
title: 'Створення Phar-архівів: Вступ'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Створення Phar-архівів: Вступ

Має бути написано в найближчому майбутньому. Перед читанням цього обов'язково прочитайте [Як використовувати Phar-архіви](phar.using.md)

Відмінним початком буде читання про [Phar::buildFromIterator()](phar.buildfromiterator.md) та про особливості вибору доступного для архівів [формату файлу](phar.fileformat.md). Хороше розуміння того, що являє собою заглушка (stub) і що вона має вирішальне значення для створення phar-архіву, і тому [Phar::setStub()](phar.setstub.md) і [Phar::createDefaultStub()](phar.createdefaultstub.md) також будуть гарною відправкою точкою. Якщо ви розповсюджуєте веб-додаток, ключовими будуть знання про [Phar::webPhar()](phar.webphar.md)и связанном с ним методе[Phar::mungServer()](phar.mungserver.md). Будь-яка програма, яка звертається до своїх власних файлів, повинна враховувати можливість використання [Phar::interceptFileFuncs()](phar.interceptfilefuncs.md)
