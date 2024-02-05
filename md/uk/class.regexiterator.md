---
navigation:
  - recursivetreeiterator.valid.md: '« RecursiveTreeIterator::valid'
  - regexiterator.accept.md: 'RegexIterator::accept »'
  - index.md: PHP Manual
  - spl.iterators.md: Ітератори
title: Клас RegexIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас RegexIterator

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

## Вступ

Цей ітератор можна використовувати для фільтрації іншого ітератора на основі регулярних виразів.

## Огляд класів

```classsynopsis

    
     class RegexIterator
    

    
     extends
      FilterIterator
     {

    /* Константы */
    
     public
     const
     int
      USE_KEY;

    public
     const
     int
      INVERT_MATCH;

    public
     const
     int
      MATCH;

    public
     const
     int
      GET_MATCH;

    public
     const
     int
      ALL_MATCHES;

    public
     const
     int
      SPLIT;

    public
     const
     int
      REPLACE;


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

Повертати всі збіги для поточного запису (дивіться [preg\_match\_all()](function.preg-match-all.md)

**`RegexIterator::GET_MATCH`**

Повертати перший збіг для поточного запису (дивіться [preg\_match()](function.preg-match.md)

**`RegexIterator::MATCH`**

Тільки виконання порівняння (фільтра) для поточного запису (дивіться [preg\_match()](function.preg-match.md)

**`RegexIterator::REPLACE`**

Заменить текущую запись (смотрите[preg\_replace()](function.preg-replace.md); Повністю поки що не реалізовано)

**`RegexIterator::SPLIT`**

Повертати розділені значення для поточного запису (див. [preg\_split()](function.preg-split.md)

## Прапори RegexIterator

**`RegexIterator::USE_KEY`**

Спеціальний прапорець: Порівняти ключ запису замість значення запису.

**`RegexIterator::INVERT_MATCH`**

Інвертує значення, що повертається [RegexIterator::accept()](regexiterator.accept.md)

## Властивості

replacement

## Зміст

-   [RegexIterator::accept](regexiterator.accept.md) \- Перевірка відповідності регулярному виразу
-   [RegexIterator::\_\_construct](regexiterator.construct.md) \- Конструктор класу RegexIterator
-   [RegexIterator::getFlags](regexiterator.getflags.md)— Отримання прапорів налаштування
-   [RegexIterator::getMode](regexiterator.getmode.md)— Повертає режим роботи
-   [RegexIterator::getPregFlags](regexiterator.getpregflags.md)— Повертає прапори регулярного вираження
-   [RegexIterator::getRegex](regexiterator.getregex.md)— Повертає рядок поточного регулярного виразу
-   [RegexIterator::setFlags](regexiterator.setflags.md) \- Установка прапорів
-   [RegexIterator::setMode](regexiterator.setmode.md)— Встановлення режиму роботи
-   [RegexIterator::setPregFlags](regexiterator.setpregflags.md) \- Завдання прапорів регулярного вираження
