Клас RecursiveTreeIterator

-   [« RecursiveRegexIterator::hasChildren](recursiveregexiterator.haschildren.html)
    
-   [RecursiveTreeIterator::beginChildren »](recursivetreeiterator.beginchildren.html)
    
-   [PHP Manual](index.html)
    
-   [Ітератори](spl.iterators.html)
    
-   Клас RecursiveTreeIterator
    

# Клас RecursiveTreeIterator

(PHP 5> = 5.3.0, PHP 7, PHP 8)

## Вступ

Дозволяє виробляти ітерації з [RecursiveIterator](class.recursiveiterator.html) для створення графічного дерева в ASCII.

## Огляд класів

```classsynopsis

     
    

    
     
      class RecursiveTreeIterator
     

     
      extends
       RecursiveIteratorIterator
     
     {
    /* Наследуемые константы */
    
     const
     int
      RecursiveIteratorIterator::LEAVES_ONLY = 0;
const
     int
      RecursiveIteratorIterator::SELF_FIRST = 1;
const
     int
      RecursiveIteratorIterator::CHILD_FIRST = 2;
const
     int
      RecursiveIteratorIterator::CATCH_GET_CHILD = 16;


    /* Константы */
    const
     int
      BYPASS_CURRENT = 4;

    const
     int
      BYPASS_KEY = 8;

    const
     int
      PREFIX_LEFT = 0;

    const
     int
      PREFIX_MID_HAS_NEXT = 1;

    const
     int
      PREFIX_MID_LAST = 2;

    const
     int
      PREFIX_END_HAS_NEXT = 3;

    const
     int
      PREFIX_END_LAST = 4;

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

-   [RecursiveTreeIterator::beginChildren](recursivetreeiterator.beginchildren.html) — Початок навігації до нащадків елемента
-   [RecursiveTreeIterator::beginIteration](recursivetreeiterator.beginiteration.html) — Початок навігації
-   [RecursiveTreeIterator::callGetChildren](recursivetreeiterator.callgetchildren.html) — Отримання дочірніх елементів
-   [RecursiveTreeIterator::callHasChildren](recursivetreeiterator.callhaschildren.html) — Перевірка, чи має поточний елемент нащадки
-   [RecursiveTreeIterator::construct](recursivetreeiterator.construct.html) - Конструктор класу RecursiveTreeIterator
-   [RecursiveTreeIterator::current](recursivetreeiterator.current.html) — Отримання поточного елемента
-   [RecursiveTreeIterator::endChildren](recursivetreeiterator.endchildren.html) — Завершення навігації за нащадками елемента
-   [RecursiveTreeIterator::endIteration](recursivetreeiterator.enditeration.html) - Завершення навігації
-   [RecursiveTreeIterator::getEntry](recursivetreeiterator.getentry.html) — Отримання піддерева, корінням якого є поточний елемент
-   [RecursiveTreeIterator::getPostfix](recursivetreeiterator.getpostfix.html) - Отримання суфікса
-   [RecursiveTreeIterator::getPrefix](recursivetreeiterator.getprefix.html) — Отримання префіксу
-   [RecursiveTreeIterator::key](recursivetreeiterator.key.html) — Отримання ключа поточного елемента
-   [RecursiveTreeIterator::next](recursivetreeiterator.next.html) — Перехід до наступного елементу
-   [RecursiveTreeIterator::nextElement](recursivetreeiterator.nextelement.html) - Наступний елемент
-   [RecursiveTreeIterator::rewind](recursivetreeiterator.rewind.html) — Переведення ітератора на початок
-   [RecursiveTreeIterator::setPostfix](recursivetreeiterator.setpostfix.html) - Встановлення постфіксу
-   [RecursiveTreeIterator::setPrefixPart](recursivetreeiterator.setprefixpart.html) - Завдання частини префікса
-   [RecursiveTreeIterator::valid](recursivetreeiterator.valid.html) - Перевірка допустимості елемента