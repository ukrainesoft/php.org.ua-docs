---
navigation:
  - simplexml.examples-errors.html: « Робота з помилками XML
  - simplexmlelement.addattribute.md: 'SimpleXMLElement::addAttribute »'
  - index.md: PHP Manual
  - book.simplexml.md: SimpleXML
title: Клас SimpleXMLElement
---
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
|  | Клас **SimpleXMLElement** тепер реалізує інтерфейси [Stringable](class.stringable.md) [Countable](class.countable.md), і [RecursiveIterator](class.recursiveiterator.md) |

## Зміст

-   [SimpleXMLElement::addAttribute](simplexmlelement.addattribute.md) - Додає атрибут до SimpleXML-елементу
-   [SimpleXMLElement::addChild](simplexmlelement.addchild.md) — Додає дочірній елемент до сайту XML
-   [SimpleXMLElement::asXML](simplexmlelement.asxml.md) — Повертає сформований XML-документ у вигляді рядка на основі елемента SimpleXML
-   [SimpleXMLElement::attributes](simplexmlelement.attributes.md) — Повертає атрибути елемента
-   [SimpleXMLElement::children](simplexmlelement.children.md) — Знаходить дочірні елементи цього вузла
-   [SimpleXMLElement::construct](simplexmlelement.construct.md) — Створення нового об'єкта SimpleXMLElement
-   [SimpleXMLElement::count](simplexmlelement.count.md) — Підраховує кількість дочірніх елементів у поточного елемента
-   [SimpleXMLElement::getDocNamespaces](simplexmlelement.getdocnamespaces.md) — Повертає простір імен, оголошених у документі
-   [SimpleXMLElement::getName](simplexmlelement.getname.md) — Отримує ім'я елемента XML
-   [SimpleXMLElement::getNamespaces](simplexmlelement.getnamespaces.md) — Повертає простір імен, які використовуються в документі
-   [SimpleXMLElement::registerXPathNamespace](simplexmlelement.registerxpathnamespace.md) — Створює префікс/простір імен контексту для наступного запиту XPath
-   [SimpleXMLElement::saveXML](simplexmlelement.savexml.md) - Псевдонім SimpleXMLElement::asXML
-   [SimpleXMLElement::toString](simplexmlelement.tostring.md) — Повертає вміст рядка
-   [SimpleXMLElement::xpath](simplexmlelement.xpath.md) — Запускає запит XPath до XML-даних
