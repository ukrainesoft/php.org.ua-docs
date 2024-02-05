---
navigation:
  - class.domdocumenttype.md: « DOMDocumentType
  - domelement.after.md: 'DOMElement::after »'
  - index.md: PHP Manual
  - book.dom.md: DOM
title: Клас DOMElement
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас DOMElement

(PHP 5, PHP 7, PHP 8)

## Огляд класів

```classsynopsis

    
     class DOMElement
    

    
     extends
      DOMNode
    

    
     implements
      DOMParentNode,

     DOMChildNode {

    /* Свойства */
    
     public
     readonly
     string
      $tagName;

    public
     string
      $className;

    public
     string
      $id;

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
    
   public __construct(string $qualifiedName, ?string $value = null, string $namespace = "")

    public after(DOMNode|string ...$nodes): void
public append(DOMNode|string ...$nodes): void
public before(DOMNode|string ...$nodes): void
public getAttribute(string $qualifiedName): string
public getAttributeNames(): array
public getAttributeNode(string $qualifiedName): DOMAttr|DOMNameSpaceNode|false
public getAttributeNodeNS(?string $namespace, string $localName): DOMAttr|DOMNameSpaceNode|null
public getAttributeNS(?string $namespace, string $localName): string
public getElementsByTagName(string $qualifiedName): DOMNodeList
public getElementsByTagNameNS(?string $namespace, string $localName): DOMNodeList
public hasAttribute(string $qualifiedName): bool
public hasAttributeNS(?string $namespace, string $localName): bool
public insertAdjacentElement(string $where, DOMElement $element): ?DOMElement
public insertAdjacentText(string $where, string $data): void
public prepend(DOMNode|string ...$nodes): void
public remove(): void
public removeAttribute(string $qualifiedName): bool
public removeAttributeNode(DOMAttr $attr): DOMAttr|false
public removeAttributeNS(?string $namespace, string $localName): void
public replaceChildren(DOMNode|string ...$nodes): void
public replaceWith(DOMNode|string ...$nodes): void
public setAttribute(string $qualifiedName, string $value): DOMAttr|bool
public setAttributeNode(DOMAttr $attr): DOMAttr|null|false
public setAttributeNodeNS(DOMAttr $attr): DOMAttr|null|false
public setAttributeNS(?string $namespace, string $qualifiedName, string $value): void
public setIdAttribute(string $qualifiedName, bool $isId): void
public setIdAttributeNode(DOMAttr $attr, bool $isId): void
public setIdAttributeNS(string $namespace, string $qualifiedName, bool $isId): void
public toggleAttribute(string $qualifiedName, ?bool $force = null): bool


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

nextElementSibling

Елемент, що прямує безпосередньо за елементом, або **`null`**

previousElementSibling

Елемент, що передує елементу, або **`null`**

schemaTypeInfo

Поки що не реалізовано, завжди повертає **`null`**

tagName

Ім'я елемента

className

Рядок, що представляє розділені коми класи елемента

id

Ідентифікатор елемента

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Додані властивості першихелементівChild, LastElementChild, ChildElementCount, попереднійElementSibling і NextElementSibling. |
| 8.0.0 | Класс**DOMElement** тепер реалізує інтерфейси [DOMParentNode](class.domparentnode.md) і [DOMChildNode](class.domchildnode.md) |

## Примітки

> **Зауваження** :
> 
> Модуль DOM працює з кодуванням UTF-8. Для роботи з іншими кодуваннями користуються функціями [mb\_convert\_encoding()](function.mb-convert-encoding.md) [UConverter::transcode()](uconverter.transcode.md) або [iconv()](function.iconv.md)

## Зміст

-   [DOMElement::after](domelement.after.md)— Додає вузли після елемента
-   [DOMElement::append](domelement.append.md)— Додає вузли після останнього дочірнього вузла
-   [DOMElement::before](domelement.before.md)— Додає вузли перед елементом
-   [DOMElement::\_\_construct](domelement.construct.md)— Створює новий екземпляр класу DOMElement
-   [DOMElement::getAttribute](domelement.getattribute.md)— Повертає значення атрибуту
-   [DOMElement::getAttributeNames](domelement.getattributenames.md)— Отримує імена атрибутів
-   [DOMElement::getAttributeNode](domelement.getattributenode.md) \- Повертає вузол атрибуту
-   [DOMElement::getAttributeNodeNS](domelement.getattributenodens.md) \- Повертає вузол атрибуту
-   [DOMElement::getAttributeNS](domelement.getattributens.md)— Повертає значення атрибуту
-   [DOMElement::getElementsByTagName](domelement.getelementsbytagname.md)— Повертає елементи на ім'я тега
-   [DOMElement::getElementsByTagNameNS](domelement.getelementsbytagnamens.md)— Отримує елементи локального імені в заданому просторі імен
-   [DOMElement::hasAttribute](domelement.hasattribute.md)— Перевіряє, чи існує атрибут
-   [DOMElement::hasAttributeNS](domelement.hasattributens.md) \- Перевіряє, чи існує заданий атрибут
-   [DOMElement::insertAdjacentElement](domelement.insertadjacentelement.md) \- Додає сусідній елемент
-   [DOMElement::insertAdjacentText](domelement.insertadjacenttext.md)— Додає сусідній текст
-   [DOMElement::prepend](domelement.prepend.md) \- Додає вузли перед першим дочірнім вузлом
-   [DOMElement::remove](domelement.remove.md) \- Видаляє елемент
-   [DOMElement::removeAttribute](domelement.removeattribute.md) \- Видаляє атрибут
-   [DOMElement::removeAttributeNode](domelement.removeattributenode.md) \- Видаляє атрибут
-   [DOMElement::removeAttributeNS](domelement.removeattributens.md) \- Видаляє атрибут
-   [DOMElement::replaceChildren](domelement.replacechildren.md)— Замінює дочірні елементи елемента
-   [DOMElement::replaceWith](domelement.replacewith.md)— Замінює елемент новими вузлами
-   [DOMElement::setAttribute](domelement.setattribute.md)— Додає новий або змінює існуючий атрибут
-   [DOMElement::setAttributeNode](domelement.setattributenode.md)— Додає новий вузол атрибуту до елементу
-   [DOMElement::setAttributeNodeNS](domelement.setattributenodens.md)— Додає новий атрибут елемент
-   [DOMElement::setAttributeNS](domelement.setattributens.md) \- Додає новий атрибут
-   [DOMElement::setIdAttribute](domelement.setidattribute.md)— Оголошує атрибут із зазначеним ім'ям тип ID
-   [DOMElement::setIdAttributeNode](domelement.setidattributenode.md)— Оголошує зазначений сайт атрибута тип ID
-   [DOMElement::setIdAttributeNS](domelement.setidattributens.md)— Оголошує атрибуту із зазначеними локальним ім'ям та URI простору імен тип ID
-   [DOMElement::toggleAttribute](domelement.toggleattribute.md) \- Перемикає атрибут
