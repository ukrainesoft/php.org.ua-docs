---
navigation:
  - reflectionuniontype.gettypes.md: '« ReflectionUnionType::getTypes'
  - reflectiongenerator.construct.md: 'ReflectionGenerator::construct »'
  - index.md: PHP Manual
  - book.reflection.md: Reflection
title: Клас ReflectionGenerator
---
# Клас ReflectionGenerator

(PHP 7, PHP 8)

## Вступ

Клас **ReflectionGenerator** повідомляє інформацію про генератор.

## Огляд класів

```classsynopsis

     
    

    
     
      final
      class ReflectionGenerator
     
     {

    /* Методы */
    
   public __construct(Generator $generator)

    public getExecutingFile(): string
public getExecutingGenerator(): Generator
public getExecutingLine(): int
public getFunction(): ReflectionFunctionAbstract
public getThis(): ?object
public getTrace(int $options = DEBUG_BACKTRACE_PROVIDE_OBJECT): array

   }
```

## список змін

| Версия | Описание |
| --- | --- |
|  | Клас тепер є остаточним (final). |

## Зміст

-   [ReflectionGenerator::construct](reflectiongenerator.construct.md) - Конструктор ReflectionGenerator
-   [ReflectionGenerator::getExecutingFile](reflectiongenerator.getexecutingfile.md) — Отримати ім'я файлу, з якого запущено генератор
-   [ReflectionGenerator::getExecutingGenerator](reflectiongenerator.getexecutinggenerator.md) — Отримати запущений об'єкт Generator
-   [ReflectionGenerator::getExecutingLine](reflectiongenerator.getexecutingline.md) — Отримати поточний рядок генератора, що виконується.
-   [ReflectionGenerator::getFunction](reflectiongenerator.getfunction.md) - Отримати ім'я функції генератора
-   [ReflectionGenerator::getThis](reflectiongenerator.getthis.md) — Отримує значення $this генератора
-   [ReflectionGenerator::getTrace](reflectiongenerator.gettrace.md) — Отримати трасування запущеного генератора
