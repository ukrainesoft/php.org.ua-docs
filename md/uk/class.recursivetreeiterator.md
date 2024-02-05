---
navigation:
  - recursiveregexiterator.haschildren.md: '« RecursiveRegexIterator::hasChildren'
  - recursivetreeiterator.beginchildren.md: 'RecursiveTreeIterator::beginChildren »'
  - index.md: PHP Manual
  - spl.iterators.md: Ітератори
title: Клас RecursiveTreeIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас RecursiveTreeIterator

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

## Вступ

Дозволяє виробляти ітерації з [RecursiveIterator](class.recursiveiterator.md) для створення графічного дерева в ASCII.

## Огляд класів

```classsynopsis

    
     class RecursiveTreeIterator
    

    
     extends
      RecursiveIteratorIterator
     {

    /* Наследуемые константы */
    
     public
     const
     int
      RecursiveIteratorIterator::LEAVES_ONLY;
public
     const
     int
      RecursiveIteratorIterator::SELF_FIRST;
public
     const
     int
      RecursiveIteratorIterator::CHILD_FIRST;
public
     const
     int
      RecursiveIteratorIterator::CATCH_GET_CHILD;


    /* Константы */
    public
     const
     int
      BYPASS_CURRENT;

    public
     const
     int
      BYPASS_KEY;

    public
     const
     int
      PREFIX_LEFT;

    public
     const
     int
      PREFIX_MID_HAS_NEXT = 1;

    public
     const
     int
      PREFIX_MID_LAST = 2;

    public
     const
     int
      PREFIX_END_HAS_NEXT = 3;

    public
     const
     int
      PREFIX_END_LAST = 4;

    public
     const
     int
      PREFIX_RIGHT = 5;


    /* Методы */
    
   public __construct(    RecursiveIterator|IteratorAggregate $iterator,    int $flags = RecursiveTreeIterator::BYPASS_KEY,    int $cachingIteratorFlags = CachingIterator::CATCH_GET_CHILD,    int $mode = RecursiveTreeIterator::SELF_FIRST)

    public beginChildren(): void
public beginIteration(): RecursiveIterator
public callGetChildren(): RecursiveIterator
public callHasChildren(): bool
public current(): mixed
public endChildren(): void
public endIteration(): void
public getEntry(): string
public getPostfix(): string
public getPrefix(): string
public key(): mixed
public next(): void
public nextElement(): void
public rewind(): void
public setPostfix(string $postfix): void
public setPrefixPart(int $part, string $value): void
public valid(): bool


    /* Наследуемые методы */
    public RecursiveIteratorIterator::beginChildren(): void
public RecursiveIteratorIterator::beginIteration(): void
public RecursiveIteratorIterator::callGetChildren(): ?RecursiveIterator
public RecursiveIteratorIterator::callHasChildren(): bool
public RecursiveIteratorIterator::current(): mixed
public RecursiveIteratorIterator::endChildren(): void
public RecursiveIteratorIterator::endIteration(): void
public RecursiveIteratorIterator::getDepth(): int
public RecursiveIteratorIterator::getInnerIterator(): RecursiveIterator
public RecursiveIteratorIterator::getMaxDepth(): int|false
public RecursiveIteratorIterator::getSubIterator(?int $level = null): ?RecursiveIterator
public RecursiveIteratorIterator::key(): mixed
public RecursiveIteratorIterator::next(): void
public RecursiveIteratorIterator::nextElement(): void
public RecursiveIteratorIterator::rewind(): void
public RecursiveIteratorIterator::setMaxDepth(int $maxDepth = -1): void
public RecursiveIteratorIterator::valid(): bool

   }
```

## Обумовлені константи

**`RecursiveTreeIterator::BYPASS_CURRENT`**

**`RecursiveTreeIterator::BYPASS_KEY`**

**`RecursiveTreeIterator::PREFIX_LEFT`**

**`RecursiveTreeIterator::PREFIX_MID_HAS_NEXT`**

**`RecursiveTreeIterator::PREFIX_MID_LAST`**

**`RecursiveTreeIterator::PREFIX_END_HAS_NEXT`**

**`RecursiveTreeIterator::PREFIX_END_LAST`**

**`RecursiveTreeIterator::PREFIX_RIGHT`**

## Зміст

-   [RecursiveTreeIterator::beginChildren](recursivetreeiterator.beginchildren.md)— Початок навігації до нащадків елемента
-   [RecursiveTreeIterator::beginIteration](recursivetreeiterator.beginiteration.md)— Початок навігації
-   [RecursiveTreeIterator::callGetChildren](recursivetreeiterator.callgetchildren.md)— Отримання дочірніх елементів
-   [RecursiveTreeIterator::callHasChildren](recursivetreeiterator.callhaschildren.md)— Перевірка, чи має поточний елемент нащадки
-   [RecursiveTreeIterator::\_\_construct](recursivetreeiterator.construct.md) \- Конструктор класу RecursiveTreeIterator
-   [RecursiveTreeIterator::current](recursivetreeiterator.current.md)— Отримання поточного елемента
-   [RecursiveTreeIterator::endChildren](recursivetreeiterator.endchildren.md)— Завершення навігації за нащадками елемента
-   [RecursiveTreeIterator::endIteration](recursivetreeiterator.enditeration.md) \- Завершення навігації
-   [RecursiveTreeIterator::getEntry](recursivetreeiterator.getentry.md)— Отримання піддерева, корінням якого є поточний елемент
-   [RecursiveTreeIterator::getPostfix](recursivetreeiterator.getpostfix.md) \- Отримання суфікса
-   [RecursiveTreeIterator::getPrefix](recursivetreeiterator.getprefix.md)— Отримання префіксу
-   [RecursiveTreeIterator::key](recursivetreeiterator.key.md)— Отримання ключа поточного елемента
-   [RecursiveTreeIterator::next](recursivetreeiterator.next.md)— Перехід до наступного елементу
-   [RecursiveTreeIterator::nextElement](recursivetreeiterator.nextelement.md) \- Наступний елемент
-   [RecursiveTreeIterator::rewind](recursivetreeiterator.rewind.md)— Переведення ітератора на початок
-   [RecursiveTreeIterator::setPostfix](recursivetreeiterator.setpostfix.md) \- Встановлення постфіксу
-   [RecursiveTreeIterator::setPrefixPart](recursivetreeiterator.setprefixpart.md) \- Завдання частини префікса
-   [RecursiveTreeIterator::valid](recursivetreeiterator.valid.md) \- Перевірка допустимості елемента
