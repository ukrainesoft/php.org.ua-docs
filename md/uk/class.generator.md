Клас Generator

-   [« Closure::fromCallable](closure.fromcallable.html)
    
-   [Generator::current »](generator.current.html)
    
-   [PHP Manual](index.html)
    
-   [Встроенные интерфейсы и классы](reserved.interfaces.html)
    
-   Клас Generator
    

# Клас Generator

(PHP 5> = 5.5.0, PHP 7, PHP 8)

## Вступ

Створення об'єктів типу **Generator** описано у розділі [Генераторы](language.generators.html)

**Застереження**

Об'єкти **Generator** не можуть бути створені за допомогою оператора [new](language.oop5.basic.html#language.oop5.basic.new)

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

Дивіться також розділ [Итераторы объектов](language.oop5.iterations.html)

## Зміст

-   [Generator::current](generator.current.html) — Отримати поточне значення генератора
-   [Generator::getReturn](generator.getreturn.html) — Отримати значення, що повертається генератором
-   [Generator::key](generator.key.html) — Отримати ключ згенерованого елемента
-   [Generator::next](generator.next.html) - Відновити роботу генератора
-   [Generator::rewind](generator.rewind.html) - Перемотати ітератор
-   [Generator::send](generator.send.html) — Передати значення у генератор
-   [Generator::throw](generator.throw.html) — Кинути виняток у генератор
-   [Generator::valid](generator.valid.html) - Перевірка, чи закритий ітератор
-   [Generator::\_\_wakeup](generator.wakeup.html) - Callback-функція серіалізації