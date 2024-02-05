---
navigation:
  - domnamednodemap.item.md: '« DOMNamedNodeMap::item'
  - class.domnode.md: DOMNode »
  - index.md: PHP Manual
  - book.dom.md: DOM
title: Клас DOMNameSpaceNode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас DOMNameSpaceNode

(PHP 5, PHP 7, PHP 8)

## Огляд класів

```classsynopsis

    
     class DOMNameSpaceNode
     {

    /* Свойства */
    
     public
     readonly
     string
      $nodeName;

    public
     readonly
     ?string
      $nodeValue;

    public
     readonly
     int
      $nodeType;

    public
     readonly
     string
      $prefix;

    public
     readonly
     ?string
      $localName;

    public
     readonly
     ?string
      $namespaceURI;

    public
     readonly
     bool
      $isConnected;

    public
     readonly
     ?DOMDocument
      $ownerDocument;

    public
     readonly
     ?DOMNode
      $parentNode;

    public
     readonly
     ?DOMElement
      $parentElement;

   }
```

## Властивості

nodeName

Кваліфікована назва вузла.

nodeValue

URI простору імен, оголошеного цим вузлом, або \*\*`null`\*\*якщо простір імен порожній.

nodeType

Тип вузла. У цьому випадку повертається [**`XML_NAMESPACE_DECL_NODE`**](dom.constants.md)

prefix

Префікс простору імен, оголошений цим вузлом.

localName

Локальна частина кваліфікованого імені цього сайту.

namespaceURI

URI простору імен, оголошеного цим вузлом, або \*\*`null`\*\*якщо воно не визначено.

isConnected

Чи пов'язаний вузол із документом.

ownerDocument

Об'єкт [DOMDocument](class.domdocument.md), пов'язаний з цим вузлом, або \*\*`null`\*\*якщо цей вузол - об'єкт класу [DOMDocument](class.domdocument.md)

parentNode

Батьківський вузол цього вузла. Якщо такого вузла немає, повертається **`null`**

parentElement

Батьківський елемент цього вузла. Якщо такого елемента немає, повертається **`null`**

## список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Додані властивості DOMNameSpaceNode::$parentElement та DOMNameSpaceNode::$isConnected. |
