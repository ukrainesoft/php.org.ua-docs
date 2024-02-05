---
navigation:
  - class.domxpath.md: « DOMXPath
  - domxpath.evaluate.md: 'DOMXPath::evaluate »'
  - index.md: PHP Manual
  - class.domxpath.md: DOMXPath
title: 'DOMXPath::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMXPath::\_\_construct

(PHP 5, PHP 7, PHP 8)

DOMXPath::\_\_construct — Створює новий об'єкт класу [DOMXPath](class.domxpath.md)

### Опис

public **DOMXPath::\_\_construct** [DOMDocument](class.domdocument.md) `$document`, bool`$registerNodeNS` **`true`**) .

Створює новий об'єкт класу [DOMXPath](class.domxpath.md)

### Список параметрів

`document`

Об'єкт класу [DOMDocument](class.domdocument.md), пов'язаний з [DOMXPath](class.domxpath.md)

`registerNodeNS`

Чи потрібно автоматично реєструвати префікси простору імен в області видимості контекстного вузла для об'єкта [DOMXPath](class.domxpath.md). Параметр допомагає уникати ручного виклику методу [DOMXPath::registerNamespace()](domxpath.registernamespace.md) для кожного простору імен у області видимості. Коли префікси простору імен конфліктують, реєструється лише префікс простору імен найближчого нащадка.
