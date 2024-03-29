---
navigation:
  - class.domnamespacenode.md: « DOMNameSpaceNode
  - domnode.appendchild.md: 'DOMNode::appendChild »'
  - index.md: PHP Manual
  - book.dom.md: DOM
title: Клас DOMNode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас DOMNode

(PHP 5, PHP 7, PHP 8)

## Огляд класів

```classsynopsis

    
     class DOMNode
     {

    /* Свойства */
    
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
    
   public appendChild(DOMNode $node): DOMNode|false
public C14N(    bool $exclusive = false,    bool $withComments = false,    ?array $xpath = null,    ?array $nsPrefixes = null): string|false
public C14NFile(    string $uri,    bool $exclusive = false,    bool $withComments = false,    ?array $xpath = null,    ?array $nsPrefixes = null): int|false
public cloneNode(bool $deep = false): DOMNode|false
public contains(DOMNode|DOMNameSpaceNode|null $other): bool
public getLineNo(): int
public getNodePath(): ?string
public getRootNode(array $options = null): DOMNode
public hasAttributes(): bool
public hasChildNodes(): bool
public insertBefore(DOMNode $node, ?DOMNode $child = null): DOMNode|false
public isDefaultNamespace(string $namespace): bool
public isEqualNode(?DOMNode $otherNode): bool
public isSameNode(DOMNode $otherNode): bool
public isSupported(string $feature, string $version): bool
public lookupNamespaceURI(?string $prefix): ?string
public lookupPrefix(string $namespace): ?string
public normalize(): void
public removeChild(DOMNode $child): DOMNode|false
public replaceChild(DOMNode $node, DOMNode $child): DOMNode|false

   }
```

## Властивості

nodeName

Повертає найточніше ім'я для поточного типу вузла

nodeValue

Значення цього вузла, залежно з його типу. Значення вузлів [DOMElement](class.domelement.md), на відміну від специфікації W3C, рівні [DOMNode::textContent](class.domnode.md#domnode.props.textcontent), а не\*\*`null`\*\*

nodeType

Повертає тип вузла. Одна з можливих [констант XML\_xxx\_NODE](dom.constants.md)

parentNode

Батьківський вузол вузла. Якщо такого вузла немає, повертає **`null`**

parentElement

Батьківський елемент поточного елемента. Якщо такого елемента немає, буде повернено значення **`null`**

childNodes

Об'єкт [DOMNodeList](class.domnodelist.md)містить всіх нащадків вузла. Якщо нащадків немає, повертається порожній об'єкт [DOMNodeList](class.domnodelist.md)

firstChild

Перший дочірній вузол вузла. Якщо такого вузла немає, повертає **`null`**

lastChild

Останній дочірній вузол цього вузла. Якщо такого вузла немає, повертає **`null`**

previousSibling

Вузол, що безпосередньо передує поточному вузлу. Якщо такого вузла немає, повертає **`null`**

nextSibling

Вузол безпосередньо наступний за вузлом. Якщо такого вузла немає, повертає **`null`**

attributes

Об'єкт [DOMNamedNodeMap](class.domnamednodemap.md), що містить атрибути вузла (тільки якщо це [DOMElement](class.domelement.md)), інакше поверне **`null`**

isConnected

Вказує, чи приєднаний вузол до документа

ownerDocument

Об'єкт [DOMDocument](class.domdocument.md), пов'язаний з вузлом, або **`null`**, якщо вузол - об'єкт класу [DOMDocument](class.domdocument.md)

namespaceURI

URI простір імен вузла або \*\*`null`\*\*якщо він не вказаний.

prefix

Префікс простору імен вузла.

localName

Повертає локальну частину кваліфікованого імені вузла.

baseURI

Абсолютний базовий URI вузла або \*\*`null`\*\*якщо реалізація не змогла отримати абсолютний URI.

textContent

Текстовий вміст вузла та його нащадків

## список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Додано властивості DOMNode::$parentElement і DOMNode::$isConnected. |
| 8.0.0 | Нереалізовані методи **DOMNode::compareDocumentPosition()** [DOMNode::isEqualNode()](domnode.isequalnode.md) **DOMNode::getFeature()** **DOMNode::setUserData()** і **DOMNode::getUserData()** були вилучені. |

## Примітки

> **Зауваження** :
> 
> Модуль DOM працює з кодуванням UTF-8. Для роботи з іншими кодуваннями користуються функціями [mb\_convert\_encoding()](function.mb-convert-encoding.md) [UConverter::transcode()](uconverter.transcode.md) або [iconv()](function.iconv.md)

## Дивіться також

-   [» Специфікація W3C елемента Node](http://www.w3.org/TR/2003/WD-DOM-Level-3-Core-20030226/DOM3-Core.md#core-ID-1950641247)

## Зміст

-   [DOMNode::appendChild](domnode.appendchild.md)— Додає новий дочірній вузол до кінця списку нащадків.
-   [DOMNode::C14N](domnode.c14n.md) \- Канонізувати вузли в рядок
-   [DOMNode::C14NFile](domnode.c14nfile.md) \- Канонізувати вузли у файл
-   [DOMNode::cloneNode](domnode.clonenode.md) \- Клонує вузол
-   [DOMNode::contains](domnode.contains.md)— Перевіряє, чи містить вузол інший вузол
-   [DOMNode::getLineNo](domnode.getlineno.md)— Отримує номер рядка вузла
-   [DOMNode::getNodePath](domnode.getnodepath.md) \- Отримання XPath вузла
-   [DOMNode::getRootNode](domnode.getrootnode.md)— Отримує кореневий вузол
-   [DOMNode::hasAttributes](domnode.hasattributes.md)— Перевіряє, чи цей вузол має атрибути.
-   [DOMNode::hasChildNodes](domnode.haschildnodes.md)— Перевіряє, чи цей вузол має нащадків.
-   [DOMNode::insertBefore](domnode.insertbefore.md)— Додає новий дочірній вузол перед вказаним вузлом
-   [DOMNode::isDefaultNamespace](domnode.isdefaultnamespace.md)— Перевіряє, чи вказаний URI простору імен вузла є простором імен за умовчанням чи ні
-   [DOMNode::isEqualNode](domnode.isequalnode.md)— Перевіряє, що обидва вузли ідентичні
-   [DOMNode::isSameNode](domnode.issamenode.md)— Вказує, чи є два вузли одним і тим самим вузлом
-   [DOMNode::isSupported](domnode.issupported.md)— Перевіряє, чи підтримується можливість у певній версії
-   [DOMNode::lookupNamespaceURI](domnode.lookupnamespaceuri.md)— Отримує URI простору імен вузла за префіксом
-   [DOMNode::lookupPrefix](domnode.lookupprefix.md)— Повертає префікс простору імен вузла із URI простору імен
-   [DOMNode::normalize](domnode.normalize.md) \- Нормалізує вузол
-   [DOMNode::removeChild](domnode.removechild.md) \- Видаляє дочірній вузол зі списку нащадків.
-   [DOMNode::replaceChild](domnode.replacechild.md) \- Замінює дочірній вузол
