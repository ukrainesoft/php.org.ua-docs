---
navigation:
  - xsl.setup.md: '" Встановлення та налаштування'
  - xsl.installation.md: Встановлення »
  - index.md: PHP Manual
  - xsl.setup.md: Встановлення та налаштування
title: Вимоги
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Вимоги

Для коректної роботи цього модуля потрібний PHP-модуль [libxml](book.libxml.md). Це означає, що також потрібна передача опції **\--with-libxml**, або до PHP 7.4 **\--enable-libxml**, хоча це вже неявно зроблено, оскільки підтримка libxml за замовчуванням включена.

Модуль використовує libxslt, який можна знайти на [» http://xmlsoft.org/XSLT/](http://xmlsoft.org/XSLT/). Необхідна версія libxslt 1.1.0 або вище.
