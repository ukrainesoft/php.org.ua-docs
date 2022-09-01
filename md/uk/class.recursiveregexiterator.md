---
navigation:
  - recursiveiteratoriterator.valid.md: '« RecursiveIteratorIterator::valid'
  - recursiveregexiterator.construct.md: 'RecursiveRegexIterator::construct »'
  - index.md: PHP Manual
  - spl.iterators.md: Ітератори
title: Клас RecursiveRegexIterator
---
# Клас RecursiveRegexIterator

(PHP 5> = 5.2.0, PHP 7, PHP 8)

## Вступ

Цей рекурсивний ітератор може фільтрувати інший рекурсивний ітератор за допомогою регулярних виразів.

## Огляд класів

```classsynopsis

     
    

    
     
      class RecursiveRegexIterator
     

     
      extends
       RegexIterator
     

     implements 
       RecursiveIterator {

    /* Наследуемые константы */
    
     const
     int
      MATCH = 0;
const
     int
      GET_MATCH = 1;
const
     int
      ALL_MATCHES = 2;
const
     int
      SPLIT = 3;
const
     int
      REPLACE = 4;
const
     int
      USE_KEY = 1;


    /* Наследуемые свойства */
    public
     ?string
      $replacement = null;


    /* Методы */
    
   public __construct(    RecursiveIterator $iterator,    string $pattern,    int $mode = RecursiveRegexIterator::MATCH,    int $flags = 0,    int $pregFlags = 0)

    public getChildren(): RecursiveRegexIterator
public hasChildren(): bool


    /* Наследуемые методы */
    public RegexIterator::accept(): bool
public RegexIterator::getFlags(): int
public RegexIterator::getMode(): int
public RegexIterator::getPregFlags(): int
public RegexIterator::getRegex(): string
public RegexIterator::setFlags(int $flags): void
public RegexIterator::setMode(int $mode): void
public RegexIterator::setPregFlags(int $pregFlags): void

    public FilterIterator::accept(): bool
public FilterIterator::current(): mixed
public FilterIterator::getInnerIterator(): Iterator
public FilterIterator::key(): mixed
public FilterIterator::next(): void
public FilterIterator::rewind(): void
public FilterIterator::valid(): bool

    public IteratorIterator::current(): mixed
public IteratorIterator::getInnerIterator(): ?Iterator
public IteratorIterator::key(): mixed
public IteratorIterator::next(): void
public IteratorIterator::rewind(): void
public IteratorIterator::valid(): bool

   }
```

## Зміст

-   [RecursiveRegexIterator::construct](recursiveregexiterator.construct.md) - Конструктор класу RecursiveRegexIterator
-   [RecursiveRegexIterator::getChildren](recursiveregexiterator.getchildren.md) — Повертає ітератор до поточного елемента
-   [RecursiveRegexIterator::hasChildren](recursiveregexiterator.haschildren.md) — Визначає, чи можлива навігація за вмістом поточного елемента
