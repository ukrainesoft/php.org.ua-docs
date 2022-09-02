---
navigation:
  - xmldiff-base.construct.md: '« XMLDiffBase::construct'
  - xmldiff-base.merge.md: 'XMLDiffBase::merge »'
  - index.md: PHP Manual
  - class.xmldiff-base.md: XMLDiffBase
title: 'XMLDiffBase::diff'
---
# XMLDiffBase::diff

(PECL xmldiff >= 0.8.0)

XMLDiffBase::diff — Порівняє два документи XML.

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
