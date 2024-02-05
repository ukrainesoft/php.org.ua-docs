---
navigation:
  - domelement.getelementsbytagname.md: '« DOMElement::getElementsByTagName'
  - domelement.hasattribute.md: 'DOMElement::hasAttribute »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::getElementsByTagNameNS'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::getElementsByTagNameNS

(PHP 5, PHP 7, PHP 8)

DOMElement::getElementsByTagNameNS — Отримує елементи локального імені в заданому просторі імен

### Опис

```methodsynopsis
public DOMElement::getElementsByTagNameNS(?string $namespace, string $localName): DOMNodeList
```

Функція вибирає всі елементи-нащадки із заданим у параметрі `localName` ім'ям та простором імен, зазначеним у параметрі `namespace`

### Список параметрів

`namespace`

URI простір імен елементів для пошуку. Спеціальне значення `"*"` відповідає всім просторам імен. Передача значення **`null`** відповідає порожньому просторі імен.

`localName`

Місцеве ім'я елементів для пошуку. Спеціальне значення `"*"` відповідає всім локальним іменам.

### Значення, що повертаються

Повертає новий об'єкт класу [DOMNodeList](class.domnodelist.md)містить всі знайдені елементи в тому порядку, в якому вони з'являються при прямому обході дерева.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.3 | `namespace` тепер допускає значення null. |

### Дивіться також

-   [DOMElement::getElementsByTagName()](domelement.getelementsbytagname.md) \- Повертає елементи на ім'я тега
