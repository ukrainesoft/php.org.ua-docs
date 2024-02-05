---
navigation:
  - phar.setup.md: '" Встановлення та налаштування'
  - phar.installation.md: Встановлення »
  - index.md: PHP Manual
  - phar.setup.md: Встановлення та налаштування
title: Вимоги
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Вимоги

Крім того, ви можете підключити модулі [zlib](book.zlib.md) і [bzip2](book.bzip2.md), щоб скористатися підтримуваною компресією phar. Також, щоб мати можливість підписування OpenSSL, має бути підключений модуль [OpenSSL](book.openssl.md)

Якщо [zend.multibyte](ini.core.md#ini.zend.multibyte) включений, то необхідно також увімкнути [zend.detect\_unicode](ini.core.md#ini.zend.detect-unicode)
