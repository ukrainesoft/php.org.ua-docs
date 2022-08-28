Клас ReflectionGenerator

-   [« ReflectionUnionType::getTypes](reflectionuniontype.gettypes.html)
    
-   [ReflectionGenerator::\_\_construct »](reflectiongenerator.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Reflection](book.reflection.html)
    
-   Клас ReflectionGenerator
    

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

| Версия | Описание                         |
|--------|----------------------------------|
|        | Клас тепер є остаточним (final). |

## Зміст

-   [ReflectionGenerator::\_\_construct](reflectiongenerator.construct.html) - Конструктор ReflectionGenerator
-   [ReflectionGenerator::getExecutingFile](reflectiongenerator.getexecutingfile.html) — Отримати ім'я файлу, з якого запущено генератор
-   [ReflectionGenerator::getExecutingGenerator](reflectiongenerator.getexecutinggenerator.html) — Отримати запущений об'єкт Generator
-   [ReflectionGenerator::getExecutingLine](reflectiongenerator.getexecutingline.html) — Отримати поточний рядок генератора, що виконується.
-   [ReflectionGenerator::getFunction](reflectiongenerator.getfunction.html) - Отримати ім'я функції генератора
-   [ReflectionGenerator::getThis](reflectiongenerator.getthis.html) — Отримує значення $this генератора
-   [ReflectionGenerator::getTrace](reflectiongenerator.gettrace.html) — Отримати трасування запущеного генератора