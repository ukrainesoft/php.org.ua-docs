---
navigation:
  - domimplementation.createdocumenttype.md: '« DOMImplementation::createDocumentType'
  - class.domnamednodemap.md: DOMNamedNodeMap »
  - index.md: PHP Manual
  - class.domimplementation.md: DOMImplementation
title: 'DOMImplementation::hasFeature'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMImplementation::hasFeature

(PHP 5, PHP 7, PHP 8)

DOMImplementation::hasFeature — Перевірка, чи реалізована певна можливість у реалізації DOM

### Опис

```methodsynopsis
public DOMImplementation::hasFeature(string $feature, string $version): bool
```

Перевіряє, чи реалізує специфічну можливість `feature`реализация DOM.

Ви можете знайти список усіх можливостей у розділі [» Узгодження](http://www.w3.org/TR/2000/REC-DOM-Level-2-Core-20001113/introduction.md#ID-Conformance)стандарта DOM.

### Список параметрів

`feature`

Тестована можливість.

`version`

Номер версії можливості, що тестується `feature`. У DOM level 2 це може бути або `2.0`, либо`1.0`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | При статичному виклику функції тепер викидається помилка [Error](class.error.md). . Раніше видавалася помилка рівня **`E_DEPRECATED`** |

### Приклади

**Приклад #1 Тестування вашої реалізації DOM**

```php
<?php

$features = array(
  'Core'           => 'Core module',
  'XML'            => 'XML module',
  'HTML'           => 'HTML module',
  'Views'          => 'Views module',
  'Stylesheets'    => 'Style Sheets module',
  'CSS'            => 'CSS module',
  'CSS2'           => 'CSS2 module',
  'Events'         => 'Events module',
  'UIEvents'       => 'User interface Events module',
  'MouseEvents'    => 'Mouse Events module',
  'MutationEvents' => 'Mutation Events module',
  'HTMLEvents'     => 'HTML Events module',
  'Range'          => 'Range module',
  'Traversal'      => 'Traversal module'
);

foreach ($features as $key => $name) {
  if (DOMImplementation::hasFeature($key, '2.0')) {
    echo "Реализует возможность $name\n";
  } else {
    echo "Возможность $name отсутствует\n";
  }
}

?>
```

### Дивіться також

-   [DOMNode::isSupported()](domnode.issupported.md) \- Перевіряє, чи підтримується можливість у певній версії
