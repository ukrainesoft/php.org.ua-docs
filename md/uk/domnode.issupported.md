---
navigation:
  - domnode.issamenode.md: '« DOMNode::isSameNode'
  - domnode.lookupnamespaceuri.md: 'DOMNode::lookupNamespaceURI »'
  - index.md: PHP Manual
  - class.domnode.md: DOMNode
title: 'DOMNode::isSupported'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMNode::isSupported

(PHP 5, PHP 7, PHP 8)

DOMNode::isSupported — Перевіряє, чи підтримується можливість у певній версії

### Опис

```methodsynopsis
public DOMNode::isSupported(string $feature, string $version): bool
```

Перевіряє, чи підтримується зазначена можливість `feature` у певній версії `version`

### Список параметрів

`feature`

Перевірювана можливість. Список можливостей наведено у прикладі до [DOMImplementation::hasFeature()](domimplementation.hasfeature.md)

`version`

Номер версії (`feature`) для перевірки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [DOMImplementation::hasFeature()](domimplementation.hasfeature.md) \- Перевірка, чи реалізована певна можливість у реалізації DOM
