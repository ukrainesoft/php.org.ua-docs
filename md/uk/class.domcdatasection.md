---
navigation:
  - domattr.isid.md: '« DOMAttr::isId'
  - domcdatasection.construct.md: 'DOMCdataSection::construct »'
  - index.md: PHP Manual
  - book.dom.md: DOM
title: Клас DOMCdataSection
---
# Клас DOMCdataSection

(PHP 5, PHP 7, PHP 8)

## Вступ

Клас **DOMCdataSection** успадковується від [DOMText](class.domtext.md) для текстового представлення конструкцій CData

## Огляд класів

```classsynopsis

     
    

    
     
      class DOMCdataSection
     

     
      extends
       DOMText
     
     {

    /* Наследуемые свойства */
    
     public
     readonly
     string
      $wholeText;

    public
     string
      $data;
public
     readonly
     int
      $length;
public
     readonly
     ?DOMElement
      $previousElementSibling;
public
     readonly
     ?DOMElement
      $nextElementSibling;

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


    /* Методы */
    
   public __construct(string $data)


    /* Наследуемые методы */
    public DOMText::isElementContentWhitespace(): bool
public DOMText::isWhitespaceInElementContent(): bool
public DOMText::splitText(int $offset): DOMText|false

    public DOMCharacterData::appendData(string $data): bool
public DOMCharacterData::deleteData(int $offset, int $count): bool
public DOMCharacterData::insertData(int $offset, string $data): bool
public DOMCharacterData::replaceData(int $offset, int $count, string $data): bool
public DOMCharacterData::substringData(int $offset, int $count): string|false

    public DOMNode::appendChild(DOMNode $node): DOMNode|false
public DOMNode::C14N(    bool $exclusive = false,    bool $withComments = false,    ?array $xpath = null,    ?array $nsPrefixes = null): string|false
public DOMNode::C14NFile(    string $uri,    bool $exclusive = false,    bool $withComments = false,    ?array $xpath = null,    ?array $nsPrefixes = null): int|false
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

## Зміст

-   [DOMCdataSection::construct](domcdatasection.construct.md) — Створює новий екземпляр класу DOMCdataSection
