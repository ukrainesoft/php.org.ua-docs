Клас SimpleXMLElement

-   [« Работа с ошибками XML](simplexml.examples-errors.html)
    
-   [SimpleXMLElement::addAttribute »](simplexmlelement.addattribute.html)
    
-   [PHP Manual](index.html)
    
-   [SimpleXML](book.simplexml.html)
    
-   Клас SimpleXMLElement
    

# Клас SimpleXMLElement

(PHP 5, PHP 7, PHP 8)

## Вступ

Є елементом у XML-документі.

## Огляд класів

```classsynopsis

     
    

    
     
      class SimpleXMLElement
     

     implements 
       Stringable,  Countable,  RecursiveIterator {

    /* Методы */
    
   public __construct(    string $data,    int $options = 0,    bool $dataIsURL = false,    string $namespaceOrPrefix = "",    bool $isPrefix = false)

    public addAttribute(string $qualifiedName, string $value, ?string $namespace = null): void
public addChild(string $qualifiedName, ?string $value = null, ?string $namespace = null): ?SimpleXMLElement
public asXML(?string $filename = null): string|bool
public attributes(?string $namespaceOrPrefix = null, bool $isPrefix = false): ?SimpleXMLElement
public children(?string $namespaceOrPrefix = null, bool $isPrefix = false): ?SimpleXMLElement
public count(): int
public getDocNamespaces(bool $recursive = false, bool $fromRoot = true): array|false
public getName(): string
public getNamespaces(bool $recursive = false): array
public registerXPathNamespace(string $prefix, string $namespace): bool
public __toString(): string
public xpath(string $expression): array|null|false

   }
```

## список змін

| Версия | Описание |
| --- | --- |
|  | Клас **SimpleXMLElement** тепер реалізує інтерфейси [Stringable](class.stringable.html) [Countable](class.countable.html), і [RecursiveIterator](class.recursiveiterator.html) |

## Зміст

-   [SimpleXMLElement::addAttribute](simplexmlelement.addattribute.html) - Додає атрибут до SimpleXML-елементу
-   [SimpleXMLElement::addChild](simplexmlelement.addchild.html) — Додає дочірній елемент до сайту XML
-   [SimpleXMLElement::asXML](simplexmlelement.asxml.html) — Повертає сформований XML-документ у вигляді рядка на основі елемента SimpleXML
-   [SimpleXMLElement::attributes](simplexmlelement.attributes.html) — Повертає атрибути елемента
-   [SimpleXMLElement::children](simplexmlelement.children.html) — Знаходить дочірні елементи цього вузла
-   [SimpleXMLElement::\_\_construct](simplexmlelement.construct.html) — Створення нового об'єкта SimpleXMLElement
-   [SimpleXMLElement::count](simplexmlelement.count.html) — Підраховує кількість дочірніх елементів у поточного елемента
-   [SimpleXMLElement::getDocNamespaces](simplexmlelement.getdocnamespaces.html) — Повертає простір імен, оголошених у документі
-   [SimpleXMLElement::getName](simplexmlelement.getname.html) — Отримує ім'я елемента XML
-   [SimpleXMLElement::getNamespaces](simplexmlelement.getnamespaces.html) — Повертає простір імен, які використовуються в документі
-   [SimpleXMLElement::registerXPathNamespace](simplexmlelement.registerxpathnamespace.html) — Створює префікс/простір імен контексту для наступного запиту XPath
-   [SimpleXMLElement::saveXML](simplexmlelement.savexml.html) - Псевдонім SimpleXMLElement::asXML
-   [SimpleXMLElement::\_\_toString](simplexmlelement.tostring.html) — Повертає вміст рядка
-   [SimpleXMLElement::xpath](simplexmlelement.xpath.html) — Запускає запит XPath до XML-даних