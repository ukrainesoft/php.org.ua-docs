---
navigation:
  - class.stdclass.md: « stdClass
  - generator.current.md: 'Generator::current »'
  - index.md: PHP Manual
  - reserved.interfaces.md: Вбудовані інтерфейси та класи
title: Клас Generator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Generator

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

## Вступ

Створення об'єктів типу **Generator** описано у розділі [Генератори](language.generators.md)

**Застереження**

Об'єкти **Generator** не можуть бути створені за допомогою оператора [new](language.oop5.basic.md#language.oop5.basic.new)

## Огляд класів

```classsynopsis

    
     final
     class Generator
    

    
     implements
      Iterator {

    /* Методы */
    
   public current(): mixed
public getReturn(): mixed
public key(): mixed
public next(): void
public rewind(): void
public send(mixed $value): mixed
public throw(Throwable $exception): mixed
public valid(): bool
public __wakeup(): void

   }
```

## Дивіться також

Смотрите также раздел[Ітератори об'єктів](language.oop5.iterations.md)

## Зміст

-   [Generator::current](generator.current.md)— Отримати поточне значення генератора
-   [Generator::getReturn](generator.getreturn.md)— Отримати значення, що повертається генератором
-   [Generator::key](generator.key.md)— Отримати ключ згенерованого елемента
-   [Generator::next](generator.next.md)— Відновити роботу генератора
-   [Generator::rewind](generator.rewind.md) \- Перемотати ітератор
-   [Generator::send](generator.send.md)— Передати значення у генератор
-   [Generator::throw](generator.throw.md)— Кинути виняток у генератор
-   [Generator::valid](generator.valid.md)— Перевіряє, чи закритий ітератор
-   [Generator::\_\_wakeup](generator.wakeup.md) \- Callback-функція серіалізації
