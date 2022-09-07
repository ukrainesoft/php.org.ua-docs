---
navigation:
  - domelement.setidattributens.md: '« DOMElement::setIdAttributeNS'
  - class.domentityreference.md: DOMEntityReference »
  - index.md: PHP Manual
  - book.dom.md: DOM
title: Клас DOMEntity
---
# Клас DOMEntity

(PHP 5, PHP 7, PHP 8)

## Вступ

Цей інтерфейс представляє відому сутність, вже розібрану чи ні, у документі XML.

## Огляд класів

```classsynopsis

     
    

    
     
      class DOMEntity
     

     
      extends
       DOMNode
     
     {

    /* Свойства */
    
     public
     readonly
     ?string
      $publicId;

    public
     readonly
     ?string
      $systemId;

    public
     readonly
     ?string
      $notationName;

    public
     readonly
     ?string
      $actualEncoding = null;

    public
     readonly
     ?string
      $encoding = null;

    public
     readonly
     ?string
      $version = null;


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
public DOMNode::C14N(    bool $exclusive = false,    bool $withComments = false,    ?array $xpath = null,    ?array $nsPrefixes = null): string|false
public DOMNode::C14NFile(    string $uri,    bool $exclusive = false,    bool $withComments = false,    ?array $xpath = null,    ?array $nsPrefixes = null): int|false
public DOMNode::cloneNode(bool $deep = false): DOMNode|false
public DOMNode::getLineNo(): int
public DOMNode::getNodePath(): ?string
public DOMNode::hasAttributes(): bool
public DOMNode::hasChildNodes(): bool
public DOMNode::insertBefore(DOMNode $node, ?DOMNode $child = null): DOMNode|false
public DOMNode::isDefaultNamespace(string $namespace): bool
public DOMNode::isSameNode(DOMNode $otherNode): bool
public DOMNode::isSupported(string $feature, string $version): bool
public DOMNode::lookupNamespaceUri(string $prefix): string
public DOMNode::lookupPrefix(string $namespace): ?string
public DOMNode::normalize(): void
public DOMNode::removeChild(DOMNode $child): DOMNode|false
public DOMNode::replaceChild(DOMNode $node, DOMNode $child): DOMNode|false

   }
```

## Властивості

publicId

Загальнодоступний ідентифікатор, що відповідає сутності або \*\*`null`\*\*якщо не заданий.

systemId

Системний ідентифікатор відповідний сутності або \*\*`null`\*\*якщо не заданий. Це може бути абсолютний URI.

notationName

Для нерозібраних об'єктів – найменування умовного позначення для сутності. Для розібраних - **`null`**

actualEncoding

Атрибут, що задає кодування, яке використовувалося при розборі сутності, для випадків, коли аналіз проводився зовнішніми методами. Атрибут має значення \*\*`null`\*\*якщо сутність знаходиться у внутрішньому підмножині або цей факт не відомий.

encoding

Атрибут, що задає кодування сутності, як і в оголошенні, коли сутність розібрана зовнішніми засобами. В іншому випадку атрибут має значення **`null`**

version

Атрибут, що задає версію елемента, якщо він розібраний зовнішніми засобами. В іншому випадку **`null`**
