---
navigation:
  - domnode.issupported.md: '« DOMNode::isSupported'
  - domnode.lookupprefix.md: 'DOMNode::lookupPrefix »'
  - index.md: PHP Manual
  - class.domnode.md: DOMNode
title: 'DOMNode::lookupNamespaceURI'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMNode::lookupNamespaceURI

(PHP 5, PHP 7, PHP 8)

DOMNode::lookupNamespaceURI — Отримує URI простору імен вузла за префіксом

### Опис

```methodsynopsis
public DOMNode::lookupNamespaceURI(?string $prefix): ?string
```

Отримує URI простору імен вузла на основі префіксу `prefix`

### Список параметрів

`prefix`

Префікс, який потрібно шукати. Якщо цей параметр дорівнює **`null`**, то метод повертає URI простору імен за умовчанням, якщо є.

### Значення, що повертаються

Повертає URI зв'язаного простору імен або \*\*`null`\*\*якщо воно не знайдено.

### Дивіться також

-   [DOMNode::lookupPrefix()](domnode.lookupprefix.md) \- Повертає префікс простору імен вузла з URI простору імен
