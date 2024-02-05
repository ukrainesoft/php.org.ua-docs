---
navigation:
  - simplexmlelement.xpath.md: '« SimpleXMLElement::xpath'
  - ref.simplexml.md: Функції SimpleXML »
  - index.md: PHP Manual
  - book.simplexml.md: SimpleXML
title: Клас SimpleXMLIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SimpleXMLIterator

(PHP 5 >= 5.1.3, PHP 7, PHP 8)

## Вступ

SimpleXMLIterator забезпечує рекурсивну ітерацію по всіх вузлах об'єкта [SimpleXMLElement](class.simplexmlelement.md)

## Огляд класів

```classsynopsis

    
     class SimpleXMLIterator
    

    
     extends
      SimpleXMLElement
     {

    /* Наследуемые методы */
    
   public SimpleXMLElement::__construct(    string $data,    int $options = 0,    bool $dataIsURL = false,    string $namespaceOrPrefix = "",    bool $isPrefix = false)

    public SimpleXMLElement::addAttribute(string $qualifiedName, string $value, ?string $namespace = null): void
public SimpleXMLElement::addChild(string $qualifiedName, ?string $value = null, ?string $namespace = null): ?SimpleXMLElement
public SimpleXMLElement::asXML(?string $filename = null): string|bool
public SimpleXMLElement::attributes(?string $namespaceOrPrefix = null, bool $isPrefix = false): ?SimpleXMLElement
public SimpleXMLElement::children(?string $namespaceOrPrefix = null, bool $isPrefix = false): ?SimpleXMLElement
public SimpleXMLElement::count(): int
public SimpleXMLElement::current(): SimpleXMLElement
public SimpleXMLElement::getDocNamespaces(bool $recursive = false, bool $fromRoot = true): array|false
public SimpleXMLElement::getName(): string
public SimpleXMLElement::getNamespaces(bool $recursive = false): array
public SimpleXMLElement::getChildren(): ?SimpleXMLElement
public SimpleXMLElement::hasChildren(): bool
public SimpleXMLElement::key(): string
public SimpleXMLElement::next(): void
public SimpleXMLElement::registerXPathNamespace(string $prefix, string $namespace): bool
public SimpleXMLElement::rewind(): void
public SimpleXMLElement::__toString(): string
public SimpleXMLElement::valid(): bool
public SimpleXMLElement::xpath(string $expression): array|null|false

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Методи ітератора (**SimpleXMLIterator::hasChildren()** **SimpleXMLIterator::getChildren()** **SimpleXMLIterator::current()** **SimpleXMLIterator::key()** **SimpleXMLIterator::next()** **SimpleXMLIterator::rewind()** **SimpleXMLIterator::valid()**) були перенесені до [SimpleXMLElement](class.simplexmlelement.md) |
| 8.0.0 | Класс**SimpleXMLIterator** тепер реалізує інтерфейс [Stringable](class.stringable.md) |
