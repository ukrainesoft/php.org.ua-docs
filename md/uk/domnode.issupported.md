Перевіряє, чи підтримується можливість у певній версії

-   [« DOMNode::isSameNode](domnode.issamenode.html)
    
-   [DOMNode::lookupNamespaceUri »](domnode.lookupnamespaceuri.html)
    
-   [PHP Manual](index.html)
    
-   [DOMNode](class.domnode.html)
    
-   Перевіряє, чи підтримується можливість у певній версії
    

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

Перевірювана можливість. Список можливостей наведено у прикладі до [DOMImplementation::hasFeature()](domimplementation.hasfeature.html)

`version`

Номер версії (`feature`) для перевірки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [DOMImplementation::hasFeature()](domimplementation.hasfeature.html) - Перевірка, чи реалізована певна можливість у реалізації DOM