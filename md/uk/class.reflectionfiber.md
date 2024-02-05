---
navigation:
  - reflectiongenerator.gettrace.md: '« ReflectionGenerator::getTrace'
  - reflectionfiber.construct.md: 'ReflectionFiber::\_\_construct »'
  - index.md: PHP Manual
  - book.reflection.md: Reflection
title: Клас ReflectionFiber
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас ReflectionFiber

(PHP 8 >= 8.1.0)

## Вступ

## Огляд класів

```classsynopsis

    
     final
     class ReflectionFiber
     {

    /* Методы */
    
   public __construct(Fiber $fiber)

    public getCallable(): callable
public getExecutingFile(): string
public getExecutingLine(): int
public getFiber(): Fiber
public getTrace(int $options = DEBUG_BACKTRACE_PROVIDE_OBJECT): array

   }
```

## Зміст

-   [ReflectionFiber::\_\_construct](reflectionfiber.construct.md)— Створює об'єкт ReflectionFiber
-   [ReflectionFiber::getCallable](reflectionfiber.getcallable.md)— Отримує об'єкт, що використовується для створення файбера.
-   [ReflectionFiber::getExecutingFile](reflectionfiber.getexecutingfile.md)— Отримує ім'я файлу поточної точки виконання
-   [ReflectionFiber::getExecutingLine](reflectionfiber.getexecutingline.md)— Отримує номер рядка поточної точки виконання
-   [ReflectionFiber::getFiber](reflectionfiber.getfiber.md)— Отримує відбитий екземпляр файбера
-   [ReflectionFiber::getTrace](reflectionfiber.gettrace.md)— Отримує зворотне трасування поточної точки виконання
