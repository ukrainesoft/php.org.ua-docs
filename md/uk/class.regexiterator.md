Клас RegexIterator

-   [« RecursiveTreeIterator::valid](recursivetreeiterator.valid.html)
    
-   [RegexIterator::accept »](regexiterator.accept.html)
    
-   [PHP Manual](index.html)
    
-   [Ітератори](spl.iterators.html)
    
-   Клас RegexIterator
    

# Клас RegexIterator

(PHP 5> = 5.2.0, PHP 7, PHP 8)

## Вступ

Цей ітератор може використовуватися для фільтрації іншого ітератора на основі регулярних виразів.

## Огляд класів

```classsynopsis

     
    

    
     
      class RegexIterator
     

     
      extends
       FilterIterator
     
     {

    /* Константы */
    
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


    /* Свойства */
    public
     ?string
      $replacement = null;


    /* Методы */
    
   public __construct(    Iterator $iterator,    string $pattern,    int $mode = RegexIterator::MATCH,    int $flags = 0,    int $pregFlags = 0)

    public accept(): bool
public getFlags(): int
public getMode(): int
public getPregFlags(): int
public getRegex(): string
public setFlags(int $flags): void
public setMode(int $mode): void
public setPregFlags(int $pregFlags): void


    /* Наследуемые методы */
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

## Обумовлені константи

## Режими роботи RegexIterator

**`RegexIterator::ALL_MATCHES`**

Повертати всі збіги для поточного запису (дивіться [pregmatchall()](function.preg-match-all.html)

**`RegexIterator::GET_MATCH`**

Повертати перший збіг для поточного запису (дивіться [pregmatch()](function.preg-match.html)

**`RegexIterator::MATCH`**

Тільки виконання порівняння (фільтра) для поточного запису (дивіться [pregmatch()](function.preg-match.html)

**`RegexIterator::REPLACE`**

Замінити поточний запис (дивіться [pregreplace()](function.preg-replace.html); Повністю поки що не реалізовано)

**`RegexIterator::SPLIT`**

Повертати розділені значення для поточного запису (див. [pregsplit()](function.preg-split.html)

## Прапори RegexIterator

**`RegexIterator::USE_KEY`**

Спеціальний прапорець: Порівняти ключ запису замість значення запису.

## Властивості

replacement

## Зміст

-   [RegexIterator::accept](regexiterator.accept.html) - Перевірка відповідності регулярному виразу
-   [RegexIterator::construct](regexiterator.construct.html) - Конструктор класу RegexIterator
-   [RegexIterator::getFlags](regexiterator.getflags.html) — Отримання прапорів налаштування
-   [RegexIterator::getMode](regexiterator.getmode.html) — Повертає режим роботи
-   [RegexIterator::getPregFlags](regexiterator.getpregflags.html) — Повертає прапори регулярного вираження
-   [RegexIterator::getRegex](regexiterator.getregex.html) — Повертає рядок поточного регулярного виразу
-   [RegexIterator::setFlags](regexiterator.setflags.html) - Установка прапорів
-   [RegexIterator::setMode](regexiterator.setmode.html) — Встановлення режиму роботи
-   [RegexIterator::setPregFlags](regexiterator.setpregflags.html) - Завдання прапорів регулярного вираження