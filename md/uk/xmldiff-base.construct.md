---
navigation:
  - class.xmldiff-base.md: « XMLDiffBase
  - xmldiff-base.diff.md: 'XMLDiffBase::diff »'
  - index.md: PHP Manual
  - class.xmldiff-base.md: XMLDiffBase
title: 'XMLDiffBase::construct'
---
# XMLDiffBase::construct

(PECL xmldiff >= 0.8.0)

XMLDiffBase::construct — Конструктор

### Опис

public **XMLDiffBase::construct**(string `$nsname`

Базовий конструктор для всіх робочих класів модуля xmldiff.

### Список параметрів

`nsname`

Вибране ім'я простору для порівняння документів. Простір за промовчанням [http://www.locus.cz/diffmark](http://www.locus.cz/diffmark) і цього достатньо, щоб уникнути конфлікту просторів імен. Використовуйте цей параметр, якщо, з якоїсь причини, ви хочете змінити значення за промовчанням.
