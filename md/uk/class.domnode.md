Клас DOMNode

-   [« DOMNamedNodeMap::item](domnamednodemap.item.md)
    
-   [DOMNode::appendChild »](domnode.appendchild.md)
    
-   [PHP Manual](index.md)
    
-   [DOM](book.dom.md)
    
-   Клас DOMNode
    

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
    
   public appendChild(DOMNode $node): DOMNode|false
public C14N(    bool $exclusive = false,    bool $withComments = false,    ?array $xpath = null,    ?array $nsPrefixes = null): string|false
public C14NFile(    string $uri,    bool $exclusive = false,    bool $withComments = false,    ?array $xpath = null,    ?array $nsPrefixes = null): int|false
public cloneNode(bool $deep = false): DOMNode|false
public getLineNo(): int
public getNodePath(): ?string
public hasAttributes(): bool
public hasChildNodes(): bool
public insertBefore(DOMNode $node, ?DOMNode $child = null): DOMNode|false
public isDefaultNamespace(string $namespace): bool
public isSameNode(DOMNode $otherNode): bool
public isSupported(string $feature, string $version): bool
public lookupNamespaceUri(string $prefix): string
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

Значення цього вузла, залежно з його типу. На відміну від специфікації W3C, значення вузлів [DOMElement](class.domelement.md) одно [DOMNode::textContent](class.domnode.html#domnode.props.textcontent), а не **`null`**

nodeType

Повертає тип цього сайту. Одна з можливих [констант XMLxxxNODE](dom.constants.md)

парентНоді

Батьківський вузол цього вузла. Якщо такого вузла немає, повертає **`null`**

childNodes

Об'єкт [DOMNodeList](class.domnodelist.md)містить всіх нащадків цього вузла. Якщо нащадків немає, повертається порожній [DOMNodeList](class.domnodelist.md)

firstChild

Перший дочірній вузол цього вузла. Якщо такого вузла немає, повертає **`null`**

lastChild

Останній дочірній вузол цього вузла. Якщо такого вузла немає, повертає **`null`**

previousSibling

Вузол, що безпосередньо передує цьому вузлу. Якщо такого вузла немає, повертає **`null`**

nextSibling

Вузол безпосередньо наступний після цього вузла. Якщо такого вузла немає, повертає **`null`**

attributes

Об'єкт [DOMNamedNodeMap](class.domnamednodemap.md), що містить атрибути цього вузла (тільки якщо це [DOMElement](class.domelement.md)), інакше поверне **`null`**

ownerDocument

Об'єкт [DOMDocument](class.domdocument.md), пов'язаний з цим вузлом, або **`null`**, якщо вузол є [DOMDocument](class.domdocument.md)

namespaceURI

URI простір імен цього вузла або \*\*`null`\*\*якщо він не вказаний.

prefix

Префікс простору імен цього вузла або \*\*`null`\*\*якщо він не вказаний.

localName

Повертає локальну частину кваліфікованого імені цього сайту.

baseURI

Абсолютний базовий URI цього вузла або \*\*`null`\*\*якщо реалізація не змогла отримати абсолютний URI.

textContent

Текстовий вміст цього вузла та його нащадків

## список змін

| Версия | Описание |
| --- | --- |
|  | Нереалізовані методи **DOMNode::compareDocumentPosition()** **DOMNode::isEqualNode()** **DOMNode::getFeature()** **DOMNode::setUserData()** і **DOMNode::getUserData()** були вилучені. |

## Примітки

> **Зауваження**
> 
> Модуль DOM використовує кодування UTF-8. Використовуйте [мбconvertencoding()](function.mb-convert-encoding.html) [UConverter::transcode()](uconverter.transcode.md) або [iconv()](function.iconv.md) для роботи з іншими кодуванням.

## Дивіться також

-   [» Специфікація W3C елемента Node](http://www.w3.org/TR/2003/WD-DOM-Level-3-Core-20030226/DOM3-Core.html#core-ID-1950641247)

## Зміст

-   [DOMNode::appendChild](domnode.appendchild.md) — Додає новий дочірній вузол до кінця списку нащадків.
-   [DOMNode::C14N](domnode.c14n.md) - Канонізувати вузли в рядок
-   [DOMNode::C14NFile](domnode.c14nfile.md) - Канонізувати вузли у файл
-   [DOMNode::cloneNode](domnode.clonenode.md) - Клонує вузол
-   [DOMNode::getLineNo](domnode.getlineno.md) - Отримати номер рядка вузла
-   [DOMNode::getNodePath](domnode.getnodepath.md) - Отримання XPath вузла
-   [DOMNode::hasAttributes](domnode.hasattributes.md) — Перевіряє, чи цей вузол має атрибути.
-   [DOMNode::hasChildNodes](domnode.haschildnodes.md) — Перевіряє, чи цей вузол має нащадків.
-   [DOMNode::insertBefore](domnode.insertbefore.md) — Додає новий дочірній вузол перед вказаним вузлом
-   [DOMNode::isDefaultNamespace](domnode.isdefaultnamespace.md) — Перевіряє, чи вказаний URI простору імен вузла є простором імен за умовчанням чи ні
-   [DOMNode::isSameNode](domnode.issamenode.md) — Вказує, чи є два вузли одним і тим самим вузлом
-   [DOMNode::isSupported](domnode.issupported.md) — Перевіряє, чи підтримується можливість у певній версії
-   [DOMNode::lookupNamespaceUri](domnode.lookupnamespaceuri.md) — Отримує URI простору імен вузла за префіксом
-   [DOMNode::lookupPrefix](domnode.lookupprefix.md) — Повертає префікс простору імен вузла із URI простору імен
-   [DOMNode::normalize](domnode.normalize.md) - Нормалізує вузол
-   [DOMNode::removeChild](domnode.removechild.md) - Видаляє дочірній вузол зі списку нащадків.
-   [DOMNode::replaceChild](domnode.replacechild.md) - Замінює дочірній вузол