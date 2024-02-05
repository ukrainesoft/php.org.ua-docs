---
navigation:
  - domelement.getattributens.md: '« DOMElement::getAttributeNS'
  - domelement.getelementsbytagnamens.md: 'DOMElement::getElementsByTagNameNS »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::getElementsByTagName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::getElementsByTagName

(PHP 5, PHP 7, PHP 8)

DOMElement::getElementsByTagName — Повертає елементи на ім'я тега

### Опис

```methodsynopsis
public DOMElement::getElementsByTagName(string $qualifiedName): DOMNodeList
```

Ця функція повертає новий екземпляр класу [DOMNodeList](class.domnodelist.md) - список всіх елементів-нащадків поточного вузла із вказаним ім'ям тега `qualifiedName`в тому порядку, в якому вони зустрічаються при обході дерева.

### Список параметрів

`qualifiedName`

Имя тега. Используйте символ`*` для всіх елементів дерева.

### Значення, що повертаються

Ця функція повертає новий об'єкт класу [DOMNodeList](class.domnodelist.md) - Список всіх відповідних елементів.

### Дивіться також

-   [DOMElement::getElementsByTagNameNS()](domelement.getelementsbytagnamens.md) \- Отримує елементи локального імені в заданому просторі імен
