---
navigation:
  - phar.fileformat.comparison.md: '« Порівняння Phar, Tar і Zip'
  - phar.fileformat.zip.md: Phar-архіви на основі zip »
  - index.md: PHP Manual
  - phar.fileformat.md: Чим відрізняється phar від tar-або zip-архіву?
title: 'Phar-архіви, засновані на tar'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Phar-архіви, засновані на tar

Архіви, засновані на форматі файлу tar, наслідують більш сучасний формат USTAR. Конструкція заголовка tar-файлу робить їх більш ефективними для доступу, ніж формат zip-файлу, і майже настільки ж ефективними, як файли формату phar. Імена файлів обмежені 255 байтами, включаючи повний шлях до phar-архіву. Обмежень кількість файлів, які у phar-архіві, заснованому на tar, немає. Ці архіви можуть бути повністю стиснуті в gzip або bzip2 форматі і, як і раніше, виконуватися модулем Phar.

Існує обмежена підтримка читання архівів у форматі обміну pax, але всі розпізнані заголовки pax (нині typeflag `x`and`g`) ігноруються. Також є обмежена підтримка архівів GNU Tar; в даний час заголовки `././@LongLink` дозволені.

Для стиснення всього архіву використовуйте [Phar::compress()](phar.compress.md). Для розпакування всього масиву використовуйте [Phar::decompress()](phar.decompress.md)
