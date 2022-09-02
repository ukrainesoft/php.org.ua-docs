---
navigation:
  - domcdatasection.construct.md: '« DOMCdataSection::construct'
  - domcharacterdata.appenddata.md: 'DOMCharacterData::appendData »'
  - index.md: PHP Manual
  - book.dom.md: DOM
title: Клас DOMCharacterData
---
# Клас DOMCharacterData

(PHP 5, PHP 7, PHP 8)

## Вступ

Представляє вузли із символьними даними. Не можна створити вузол із цього класу безпосередньо, вузли створюються з успадкованих від цього класів.

## Огляд класів

```classsynopsis

     
    

    
     
      class DOMCharacterData
     

     
      extends
       DOMNode
     

     implements 
       DOMChildNode {

    /* Свойства */
    
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
    
   public appendData(string $data): bool
public deleteData(int $offset, int $count): bool
public insertData(int $offset, string $data): bool
public replaceData(int $offset, int $count, string $data): bool
public substringData(int $offset, int $count): string|false


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

data

Вміст вузла.

length

Довжина вмісту.

nextElementSibling

Елемент безпосередньо наступний за даним елементом або **`null`**

previousElementSibling

Елемент попередній елементу або **`null`**

## список змін

| Версия | Описание |
| --- | --- |
|  | Додані властивості nextElementSibling і previousElementSibling. |
|  | Клас **DOMCharacterData** тепер реалізує інтерфейс [DOMChildNode](class.domchildnode.md) |

## Дивіться також

-   [» Специфікація W3C символьних даних](http://www.w3.org/TR/2003/WD-DOM-Level-3-Core-20030226/DOM3-Core.md#core-ID-FF21A306)

## Зміст

-   [DOMCharacterData::appendData](domcharacterdata.appenddata.md) — Додати рядок до кінця символьних даних вузла
-   [DOMCharacterData::deleteData](domcharacterdata.deletedata.md) — Видалити діапазон символів із вузла
-   [DOMCharacterData::insertData](domcharacterdata.insertdata.md) — Вставити рядок у вказану 16-бітну позицію
-   [DOMCharacterData::replaceData](domcharacterdata.replacedata.md) — Замінити підрядок у вузлі типу DOMCharacterData
-   [DOMCharacterData::substringData](domcharacterdata.substringdata.md) — Витягує певний діапазон даних із вузла
