---
navigation:
  - domxpath.query.md: '« DOMXPath::query'
  - domxpath.registerphpfunctions.md: 'DOMXPath::registerPhpFunctions »'
  - index.md: PHP Manual
  - class.domxpath.md: DOMXPath
title: 'DOMXPath::registerNamespace'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMXPath::registerNamespace

(PHP 5, PHP 7, PHP 8)

DOMXPath::registerNamespace — Реєструє простір імен з об'єктом [DOMXPath](class.domxpath.md)

### Опис

```methodsynopsis
public DOMXPath::registerNamespace(string $prefix, string $namespace): bool
```

Реєструє URI простору імен `namespace`и префикс`prefix` з об'єктом DOMXPath.

### Список параметрів

`prefix`

Префікс.

`namespace`

URI простір імен.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
