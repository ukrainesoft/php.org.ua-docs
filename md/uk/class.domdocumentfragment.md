---
navigation:
  - domdocument.xinclude.md: '« DOMDocument::xinclude'
  - domdocumentfragment.append.md: 'DOMDocumentFragment::append »'
  - index.md: PHP Manual
  - book.dom.md: DOM
title: Клас DOMDocumentFragment
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас DOMDocumentFragment

(PHP 5, PHP 7, PHP 8)

## Огляд класів

```classsynopsis

    
     class DOMDocumentFragment
    

    
     extends
      DOMNode
    

    
     implements
      DOMParentNode {

    /* Свойства */
    
     public
     readonly
     ?DOMElement
      $firstElementChild;

    public
     readonly
     ?DOMElement
      $lastElementChild;

    public
     readonly
     int
      $childElementCount;


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


    /* Методы */
    
   public __construct()

    public append(DOMNode|string ...$nodes): void
public appendXML(string $data): bool
public prepend(DOMNode|string ...$nodes): void
public replaceChildren(DOMNode|string ...$nodes): void


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

childElementCount

Кількість дочірніх елементів.

firstElementChild

Перший дочірній елемент або **`null`**

lastElementChild

Останній дочірній елемент або **`null`**

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Додані властивості першихелементівChild, LastElementChild і ChildElementCount. |
| 8.0.0 | Класс**DOMDocumentFragment** тепер реалізує інтерфейс [DOMParentNode](class.domparentnode.md) |

## Зміст

-   [DOMDocumentFragment::append](domdocumentfragment.append.md)— Додає вузли після останнього дочірнього вузла
-   [DOMDocumentFragment::appendXML](domdocumentfragment.appendxml.md)— Додавання необроблених даних XML
-   [DOMDocumentFragment::\_\_construct](domdocumentfragment.construct.md) \- Конструктор об'єкта DOMDocumentFragment
-   [DOMDocumentFragment::prepend](domdocumentfragment.prepend.md) \- Додає вузли перед першим дочірнім вузлом
-   [DOMDocumentFragment::replaceChildren](domdocumentfragment.replacechildren.md)— Замінює дочірні елементи фрагмента
