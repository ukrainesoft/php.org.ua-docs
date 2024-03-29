---
navigation:
  - domdocumentfragment.replacechildren.md: '« DOMDocumentFragment::replaceChildren'
  - class.domelement.md: DOMElement »
  - index.md: PHP Manual
  - book.dom.md: DOM
title: Клас DOMDocumentType
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас DOMDocumentType

(PHP 5, PHP 7, PHP 8)

## Вступ

Кожен об'єкт [DOMDocument](class.domdocument.md) є атрибут `doctype`значення якого — або **`null`**, або об'єкт класу **DOMDocumentType**

## Огляд класів

```classsynopsis

    
     class DOMDocumentType
    

    
     extends
      DOMNode
     {

    /* Свойства */
    
     public
     readonly
     string
      $name;

    public
     readonly
     DOMNamedNodeMap
      $entities;

    public
     readonly
     DOMNamedNodeMap
      $notations;

    public
     readonly
     string
      $publicId;

    public
     readonly
     string
      $systemId;

    public
     readonly
     ?string
      $internalSubset;


    /* Наследуемые свойства */
    public
     readonly
     string
      $nodeName;
public
     ?string
      $nodeValue;
public
     readonly
     int
      $nodeType;
public
     readonly
     ?DOMNode
      $parentNode;
public
     readonly
     ?DOMElement
      $parentElement;
public
     readonly
     DOMNodeList
      $childNodes;
public
     readonly
     ?DOMNode
      $firstChild;
public
     readonly
     ?DOMNode
      $lastChild;
public
     readonly
     ?DOMNode
      $previousSibling;
public
     readonly
     ?DOMNode
      $nextSibling;
public
     readonly
     ?DOMNamedNodeMap
      $attributes;
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
     ?string
      $namespaceURI;
public
     string
      $prefix;
public
     readonly
     ?string
      $localName;
public
     readonly
     ?string
      $baseURI;
public
     string
      $textContent;


    /* Наследуемые методы */
    
   public DOMNode::appendChild(DOMNode $node): DOMNode|false
public DOMNode::C14N(    bool $exclusive = false,    bool $withComments = false,    ?array $xpath = null,    ?array $nsPrefixes = null): string|false
public DOMNode::C14NFile(    string $uri,    bool $exclusive = false,    bool $withComments = false,    ?array $xpath = null,    ?array $nsPrefixes = null): int|false
public DOMNode::cloneNode(bool $deep = false): DOMNode|false
public DOMNode::contains(DOMNode|DOMNameSpaceNode|null $other): bool
public DOMNode::getLineNo(): int
public DOMNode::getNodePath(): ?string
public DOMNode::getRootNode(array $options = null): DOMNode
public DOMNode::hasAttributes(): bool
public DOMNode::hasChildNodes(): bool
public DOMNode::insertBefore(DOMNode $node, ?DOMNode $child = null): DOMNode|false
public DOMNode::isDefaultNamespace(string $namespace): bool
public DOMNode::isEqualNode(?DOMNode $otherNode): bool
public DOMNode::isSameNode(DOMNode $otherNode): bool
public DOMNode::isSupported(string $feature, string $version): bool
public DOMNode::lookupNamespaceURI(?string $prefix): ?string
public DOMNode::lookupPrefix(string $namespace): ?string
public DOMNode::normalize(): void
public DOMNode::removeChild(DOMNode $child): DOMNode|false
public DOMNode::replaceChild(DOMNode $node, DOMNode $child): DOMNode|false

   }
```

## Властивості

publicId

Загальнодоступний ідентифікатор зовнішнього підмножини типів.

systemId

Системний ідентифікатор зовнішнього підмножини типів. Це може бути абсолютний URI.

name

Ім'я DTD, тобто ім'я, наступне відразу за ключовим словом `DOCTYPE`

entities

Об'єкт класу [DOMNamedNodeMap](class.domnamednodemap.md), Що містить основні елементи, внутрішні та зовнішні, оголошені в DTD.

notations

Об'єкт класу [DOMNamedNodeMap](class.domnamednodemap.md)містить позначення, оголошені в DTD.

internalSubset

Внутрішнє підмножина у вигляді рядка або \*\*`null`\*\*якщо його немає. Воно не повинно містити розділових квадратних дужок.
