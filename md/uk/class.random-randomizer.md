---
navigation:
  - function.srand.md: « srand
  - random-randomizer.construct.md: 'Random\\Randomizer::\_\_construct »'
  - index.md: PHP Manual
  - book.random.md: Random
title: Клас Random\\Randomizer
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Random\\Randomizer

(PHP 8 >= 8.2.0)

## Вступ

Надає високорівневий API для випадковості, що забезпечується класом [Random\\Engine](class.random-engine.md)

## Огляд класів

```classsynopsis

    
     final
     class Random\Randomizer
     {

    /* Свойства */
    
     public
     readonly
     Random\Engine
      $engine;


    /* Методы */
    
   public __construct(?Random\Engine $engine = null)

    public getBytes(int $length): string
public getBytesFromString(string $string, int $length): string
public getFloat(float $min, float $max, Random\IntervalBoundary $boundary = Random\IntervalBoundary::ClosedOpen): float
public getInt(int $min, int $max): int
public nextFloat(): float
public nextInt(): int
public pickArrayKeys(array $array, int $num): array
public __serialize(): array
public shuffleArray(array $array): array
public shuffleBytes(string $bytes): string
public __unserialize(array $data): void

   }
```

## Властивості

engine

Низькорівневе джерело випадкової послідовності для методів [Random\\Randomizer](class.random-randomizer.md)

## Зміст

-   [Random\\Randomizer::\_\_construct](random-randomizer.construct.md)— Створює новий об'єкт Randomizer
-   [Random\\Randomizer::getBytes](random-randomizer.getbytes.md)— Отримує випадкові байти
-   [Random\\Randomizer::getBytesFromString](random-randomizer.getbytesfromstring.md)— Отримує випадкові байти з вихідного рядка
-   [Random\\Randomizer::getFloat](random-randomizer.getfloat.md)— Отримує рівномірно обране число з плаваючою точкою
-   [Random\\Randomizer::getInt](random-randomizer.getint.md)— Отримує рівномірно вибране ціле число
-   [Random\\Randomizer::nextFloat](random-randomizer.nextfloat.md)— Отримує число з точкою, що плаває, з відкритого праворуч інтервалу\[
-   [Random\\Randomizer::nextInt](random-randomizer.nextint.md)— Отримує ціле позитивне число
-   [Random\\Randomizer::pickArrayKeys](random-randomizer.pickarraykeys.md) \- Вибирає випадкові ключі масиву
-   [Random\\Randomizer::\_\_serialize](random-randomizer.serialize.md) \- Серіалізує об'єкт Randomizer
-   [Random\\Randomizer::shuffleArray](random-randomizer.shufflearray.md)— Отримує перестановку масиву
-   [Random\\Randomizer::shuffleBytes](random-randomizer.shufflebytes.md)— Отримує байтову перестановку рядка
-   [Random\\Randomizer::\_\_unserialize](random-randomizer.unserialize.md)— Десеріалізує параметр data в об'єкті Randomizer
