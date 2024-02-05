---
navigation:
  - class.xmldiff-base.md: « XMLDiff\\Base
  - xmldiff-base.diff.md: 'XMLDiff\\Base::diff »'
  - index.md: PHP Manual
  - class.xmldiff-base.md: XMLDiff\\Base
title: 'XMLDiff\\Base::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLDiff\\Base::\_\_construct

(PECL xmldiff >= 0.8.0)

XMLDiff\\Base::\_\_construct — Конструктор

### Опис

public **XMLDiff\\Base::\_\_construct**(string`$nsname`) .

Базовий конструктор для всіх робочих класів модуля xmldiff.

### Список параметрів

`nsname`

Вибране ім'я простору для порівняння документів. Простір за промовчанням [http://www.locus.cz/diffmark](http://www.locus.cz/diffmark) і цього достатньо, щоб уникнути конфлікту просторів імен. Використовуйте цей параметр, якщо, з якоїсь причини, ви хочете змінити значення за промовчанням.
