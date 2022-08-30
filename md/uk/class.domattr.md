Клас DOMAttr

-   [« Приклади](dom.examples.md)
    
-   [DOMAttr::construct »](domattr.construct.md)
    
-   [PHP Manual](index.md)
    
-   [DOM](book.dom.md)
    
-   Клас DOMAttr
    

# Клас [DOMAttr](class.domattr.md)

(PHP 5, PHP 7, PHP 8)

## Вступ

**DOMAttr** надає атрибут в об'єкті [DOMElement](class.domelement.md)

## Огляд класів

```classsynopsis

     
    

    
     
      class DOMAttr
     

     
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
     bool
      $specified = true;

    public
     string
      $value;

    public
     readonly
     ?DOMElement
      $ownerElement;

    public
     readonly
     mixed
      $schemaTypeInfo = null;


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


    /* Методы */
    
   public __construct(string $name, string $value = "")

    public isId(): bool


    /* Наследуемые методы */
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

## Властивості

name

Ім'я атрибуту.

ownerElement

Елемент, який містить атрибут або **`null`**

schemaTypeInfo

Ще не реалізовано, повертає **`null`**

specified

Ще не реалізовано, повертає **`null`**

value

Значення атрибуту.

## Дивіться також

-   [» Спецификация W3C для Attr](http://www.w3.org/TR/2003/WD-DOM-Level-3-Core-20030226/DOM3-Core.html#core-ID-637646024)

## Зміст

-   [DOMAttr::construct](domattr.construct.md) - Створює екземпляр класу DOMAttr
-   [DOMAttr::isId](domattr.isid.md) — Перевіряє, чи є атрибут певним ідентифікатором