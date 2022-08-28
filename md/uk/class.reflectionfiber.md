Клас ReflectionFiber

-   [« ReflectionGenerator::getTrace](reflectiongenerator.gettrace.html)
    
-   [ReflectionFiber::\_\_construct »](reflectionfiber.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Reflection](book.reflection.html)
    
-   Клас ReflectionFiber
    

# Клас ReflectionFiber

(PHP 8> = 8.1.0)

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

-   [ReflectionFiber::\_\_construct](reflectionfiber.construct.html) — Створює об'єкт ReflectionFiber
-   [ReflectionFiber::getCallable](reflectionfiber.getcallable.html) — Отримує об'єкт, що використовується для створення файбера.
-   [ReflectionFiber::getExecutingFile](reflectionfiber.getexecutingfile.html) — Отримує ім'я файлу поточної точки виконання
-   [ReflectionFiber::getExecutingLine](reflectionfiber.getexecutingline.html) — Отримує номер рядка поточної точки виконання
-   [ReflectionFiber::getFiber](reflectionfiber.getfiber.html) — Отримує відбитий екземпляр файбера
-   [ReflectionFiber::getTrace](reflectionfiber.gettrace.html) — Отримує зворотне трасування поточної точки виконання