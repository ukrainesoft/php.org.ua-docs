---
navigation:
  - domprocessinginstruction.construct.md: '« DOMProcessingInstruction::\_\_construct'
  - domtext.construct.md: 'DOMText::\_\_construct »'
  - index.md: PHP Manual
  - book.dom.md: DOM
title: Клас DOMText
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас DOMText

(PHP 5, PHP 7, PHP 8)

## Вступ

Класс**DOMText**наследуется от[DOMCharacterData](class.domcharacterdata.md) і представляє текстовий вміст [DOMElement](class.domelement.md) або [DOMAttr](class.domattr.md)

## Огляд класів

```classsynopsis

    
     class DOMText
    

    
     extends
      DOMCharacterData
     {

    /* Свойства */
    
     public
     readonly
     string
      $wholeText;


    /* Наследуемые свойства */
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
    
   public __construct(string $data = "")

    public isElementContentWhitespace(): bool
public isWhitespaceInElementContent(): bool
public splitText(int $offset): DOMText|false


    /* Наследуемые методы */
    public DOMCharacterData::after(DOMNode|string ...$nodes): void
public DOMCharacterData::appendData(string $data): true
public DOMCharacterData::before(DOMNode|string ...$nodes): void
public DOMCharacterData::deleteData(int $offset, int $count): bool
public DOMCharacterData::insertData(int $offset, string $data): bool
public DOMCharacterData::remove(): void
public DOMCharacterData::replaceData(int $offset, int $count, string $data): bool
public DOMCharacterData::replaceWith(DOMNode|string ...$nodes): void
public DOMCharacterData::substringData(int $offset, int $count): string|false

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

wholeText

Містить весь текст суміжних текстових вузлів (не розділені іншими елементами, коментарями або інструкціями).

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Нереалізований метод \*\*DOMText::replaceWholeText()\*\*був видалений. |

## Зміст

-   [DOMText::\_\_construct](domtext.construct.md)— Створює об'єкт класу DOMText
-   [DOMText::isElementContentWhitespace](domtext.iselementcontentwhitespace.md)— Повертає, чи містить текстовий вузол пробіл у вмісті елемента
-   [DOMText::isWhitespaceInElementContent](domtext.iswhitespaceinelementcontent.md)— Визначає, чи містить текстовий вузол пробіли у вмісті
-   [DOMText::splitText](domtext.splittext.md)— Поділяє вузол на два, починаючи із заданої позиції
