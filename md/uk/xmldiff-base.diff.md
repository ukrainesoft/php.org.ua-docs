---
navigation:
  - xmldiff-base.construct.md: '« XMLDiff\\Base::\_\_construct'
  - xmldiff-base.merge.md: 'XMLDiff\\Base::merge »'
  - index.md: PHP Manual
  - class.xmldiff-base.md: XMLDiff\\Base
title: 'XMLDiff\\Base::diff'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLDiff\\Base::diff

(PECL xmldiff >= 0.8.0)

XMLDiff\\Base::diff — Порівняє два документи XML.

### Опис

```methodsynopsis
abstract public XMLDiff\Base::diff(mixed $from, mixed $to): mixed
```

Абстрактний метод порівняння для реалізації у класах спадкоємців.

Головне завдання цього - створення списку відмінностей двох документів. Порядок вхідних параметрів є важливим, оскільки від нього залежить результат.

### Список параметрів

`from`

Початковий документ XML.

`to`

XML документ, з яким проводиться порівняння.

### Значення, що повертаються

Залежить від реалізації.
