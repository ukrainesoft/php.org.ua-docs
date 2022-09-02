---
navigation:
  - class.domdocumenttype.md: « DOMDocumentType
  - domelement.construct.md: 'DOMElement::construct »'
  - index.md: PHP Manual
  - book.dom.md: DOM
title: Клас DOMElement
---
# Клас DOMElement

(PHP 5, PHP 7, PHP 8)

## Огляд класів

```classsynopsis

     
    

    
     
      class DOMElement
     

     
      extends
       DOMNode
     

     implements 
       DOMParentNode,  DOMChildNode {

    /* Свойства */
    
     public
     readonly
     string
      $tagName;

    public
     readonly
     mixed
      $schemaTypeInfo = null;

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

    public
     readonly
     ?DOMElement
      $previousElementSibling;

    public
     readonly
     ?DOMElement
      $nextElementSibling;


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
    
   public __construct(string $qualifiedName, ?string $value = null, string $namespace = "")

    public getAttribute(string $qualifiedName): string
public getAttributeNode(string $qualifiedName): DOMAttr|DOMNameSpaceNode|false
public getAttributeNodeNS(?string $namespace, string $localName): DOMAttr|DOMNameSpaceNode|null
public getAttributeNS(?string $namespace, string $localName): string
public getElementsByTagName(string $qualifiedName): DOMNodeList
public getElementsByTagNameNS(?string $namespace, string $localName): DOMNodeList
public hasAttribute(string $qualifiedName): bool
public hasAttributeNS(?string $namespace, string $localName): bool
public removeAttribute(string $qualifiedName): bool
public removeAttributeNode(DOMAttr $attr): DOMAttr|false
public removeAttributeNS(?string $namespace, string $localName): void
public setAttribute(string $qualifiedName, string $value): DOMAttr|bool
public setAttributeNode(DOMAttr $attr): DOMAttr|null|false
public setAttributeNodeNS(DOMAttr $attr): DOMAttr|null|false
public setAttributeNS(?string $namespace, string $qualifiedName, string $value): void
public setIdAttribute(string $qualifiedName, bool $isId): void
public setIdAttributeNode(DOMAttr $attr, bool $isId): void
public setIdAttributeNS(string $namespace, string $qualifiedName, bool $isId): void


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

childElementCount

Кількість дочірніх елементів.

першийЕlementChild

Перший дочірній елемент або **`null`**

останнійеlementChild

Останній дочірній елемент або **`null`**

nextElementSibling

Елемент безпосередньо наступний за даним елементом або **`null`**

previousElementSibling

Елемент попередній елементу або **`null`**

schemaTypeInfo

Поки що не реалізовано, завжди повертає **`null`**

tagName

Ім'я елемента

## список змін

| Версия | Описание |
| --- | --- |
|  | Додані властивості першихелементівChild, LastElementChild, ChildElementCount, попереднійElementSibling і NextElementSibling. |
|  | Клас **DOMElement** тепер реалізує інтерфейс [DOMParentNode](class.domparentnode.md) і [DOMChildNode](class.domchildnode.md) |

## Примітки

> **Зауваження**
> 
> Модуль DOM використовує кодування UTF-8. Використовуйте [мбconvertencoding()](function.mb-convert-encoding.md) [UConverter::transcode()](uconverter.transcode.md) або [iconv()](function.iconv.md) для роботи з іншими кодуванням.

## Зміст

-   [DOMElement::construct](domelement.construct.md) — Створює новий екземпляр класу DOMElement
-   [DOMElement::getAttribute](domelement.getattribute.md) — Повертає значення атрибуту
-   [DOMElement::getAttributeNode](domelement.getattributenode.md) - Повертає вузол атрибуту
-   [DOMElement::getAttributeNodeNS](domelement.getattributenodens.md) - Повертає вузол атрибуту
-   [DOMElement::getAttributeNS](domelement.getattributens.md) — Повертає значення атрибуту
-   [DOMElement::getElementsByTagName](domelement.getelementsbytagname.md) — Повертає елементи на ім'я тега
-   [DOMElement::getElementsByTagNameNS](domelement.getelementsbytagnamens.md) — Отримання елементів локального імені в заданому просторі імен
-   [DOMElement::hasAttribute](domelement.hasattribute.md) — Перевіряє, чи існує атрибут
-   [DOMElement::hasAttributeNS](domelement.hasattributens.md) - Перевіряє, чи існує заданий атрибут
-   [DOMElement::removeAttribute](domelement.removeattribute.md) - Видаляє атрибут
-   [DOMElement::removeAttributeNode](domelement.removeattributenode.md) - Видаляє атрибут
-   [DOMElement::removeAttributeNS](domelement.removeattributens.md) - Видаляє атрибут
-   [DOMElement::setAttribute](domelement.setattribute.md) — Додає новий або змінює існуючий атрибут
-   [DOMElement::setAttributeNode](domelement.setattributenode.md) — Додає новий вузол атрибуту до елементу
-   [DOMElement::setAttributeNodeNS](domelement.setattributenodens.md) — Додає новий атрибут елемент
-   [DOMElement::setAttributeNS](domelement.setattributens.md) - Додає новий атрибут
-   [DOMElement::setIdAttribute](domelement.setidattribute.md) — Оголошує атрибут, вказаний ім'ям, з ідентифікатором типу
-   [DOMElement::setIdAttributeNode](domelement.setidattributenode.md) — Оголошує атрибут, вказаний вузлом, з ідентифікатором типу
-   [DOMElement::setIdAttributeNS](domelement.setidattributens.md) — Оголошує атрибут, вказаний локальним ім'ям та URI простору імен, з ідентифікатором типу
