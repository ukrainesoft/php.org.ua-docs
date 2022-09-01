---
navigation:
  - simplexmlelement.xpath.md: '« SimpleXMLElement::xpath'
  - simplexmliterator.current.md: 'SimpleXMLIterator::current »'
  - index.md: PHP Manual
  - book.simplexml.md: SimpleXML
title: Клас SimpleXMLIterator
---
# Клас SimpleXMLIterator

(PHP 5> = 5.1.3, PHP 7, PHP 8)

## Вступ

SimpleXMLIterator забезпечує рекурсивну ітерацію по всіх вузлах об'єкта [SimpleXMLElement](class.simplexmlelement.md)

## Огляд класів

```classsynopsis

     
    

    
     
      class SimpleXMLIterator
     

     
      extends
       SimpleXMLElement
     
     {

    /* Методы */
    
   public current(): mixed
public getChildren(): SimpleXMLIterator
public hasChildren(): bool
public key(): mixed
public next(): void
public rewind(): void
public valid(): bool


    /* Наследуемые методы */
    public SimpleXMLElement::addAttribute(string $qualifiedName, string $value, ?string $namespace = null): void
public SimpleXMLElement::addChild(string $qualifiedName, ?string $value = null, ?string $namespace = null): ?SimpleXMLElement
public SimpleXMLElement::asXML(?string $filename = null): string|bool
public SimpleXMLElement::attributes(?string $namespaceOrPrefix = null, bool $isPrefix = false): ?SimpleXMLElement
public SimpleXMLElement::children(?string $namespaceOrPrefix = null, bool $isPrefix = false): ?SimpleXMLElement
public SimpleXMLElement::count(): int
public SimpleXMLElement::getDocNamespaces(bool $recursive = false, bool $fromRoot = true): array|false
public SimpleXMLElement::getName(): string
public SimpleXMLElement::getNamespaces(bool $recursive = false): array
public SimpleXMLElement::registerXPathNamespace(string $prefix, string $namespace): bool
public SimpleXMLElement::__toString(): string
public SimpleXMLElement::xpath(string $expression): array|null|false

   }
```

## список змін

| Версия | Описание |
| --- | --- |
|  | Клас **SimpleXMLIterator** тепер реалізує інтерфейс [Stringable](class.stringable.md) |

## Зміст

-   [SimpleXMLIterator::current](simplexmliterator.current.md) — Повертає поточний елемент
-   [SimpleXMLIterator::getChildren](simplexmliterator.getchildren.md) — Повертає вкладені елементи поточного елемента
-   [SimpleXMLIterator::hasChildren](simplexmliterator.haschildren.md) — Перевіряє, чи поточний елемент має вкладені елементи.
-   [SimpleXMLIterator::key](simplexmliterator.key.md) — Повертає поточний ключ
-   [SimpleXMLIterator::next](simplexmliterator.next.md) — Переміщує ітератор до наступного елементу
-   [SimpleXMLIterator::rewind](simplexmliterator.rewind.md) — Повертає ітератор до першого елементу
-   [SimpleXMLIterator::valid](simplexmliterator.valid.md) — Перевіряє, чи поточний елемент є допустимим
