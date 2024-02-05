---
navigation:
  - xmldiff-base.diff.md: '« XMLDiff\\Base::diff'
  - class.xmldiff-dom.md: XMLDiff\\DOM »
  - index.md: PHP Manual
  - class.xmldiff-base.md: XMLDiff\\Base
title: 'XMLDiff\\Base::merge'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLDiff\\Base::merge

(PECL xmldiff >= 0.8.0)

XMLDiff\\Base::merge — Створює новий документ XML, ґрунтуючись на інформації про його відмінність від іншого

### Опис

```methodsynopsis
abstract public XMLDiff\Base::merge(mixed $src, mixed $diff): mixed
```

Абстрактний метод порівняння для реалізації у класах спадкоємців.

Основна мета методу - створення нового документа на основі інформації про відмінності двох документів.

### Список параметрів

`src`

Початковий документ XML.

`diff`

Документ, створений методом, що реалізує абстрактний метод XMLDiff\\Base::diff.

### Значення, що повертаються

Залежить від реалізації.
