Клас Fiber

-   [« Generator::\_\_wakeup](generator.wakeup.html)
    
-   [Fiber::\_\_construct »](fiber.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Встроенные интерфейсы и классы](reserved.interfaces.html)
    
-   Клас Fiber
    

# Клас Fiber

(PHP 8> = 8.1.0)

## Вступ

Файбери є перериваються функції повного циклу. Файбери можуть бути припинені з будь-якого місця циклу, призупиняючи виконання у файбері доти, доки файбер не буде відновлено в майбутньому.

## Огляд класів

```classsynopsis

     
    

    
     
      final
      class Fiber
     
     {

    /* Методы */
    
   public __construct(callable $callback)

    public start(mixed ...$args): mixed
public resume(mixed $value = null): mixed
public throw(Throwable $exception): mixed
public getReturn(): mixed
public isStarted(): bool
public isSuspended(): bool
public isRunning(): bool
public isTerminated(): bool
public static suspend(mixed $value = null): mixed
public static getCurrent(): ?Fiber

   }
```

## Дивіться також

[Обзор файберов](language.fibers.html)

## Зміст

-   [Fiber::\_\_construct](fiber.construct.html) - Створює новий екземпляр Fiber
-   [Fiber::start](fiber.start.html) - Починає виконання волокна
-   [Fiber::resume](fiber.resume.html) — Відновлює виконання файбера зі значенням
-   [Fiber::throw](fiber.throw.html) — Відновлює виконання файбера за винятком
-   [Fiber::getReturn](fiber.getreturn.html) — Отримує значення, яке повертається файбером
-   [Fiber::isStarted](fiber.isstarted.html) — Визначає, чи запущено файбер
-   [Fiber::isSuspended](fiber.issuspended.html) — Визначає, чи зупинено файбер
-   [Fiber::isRunning](fiber.isrunning.html) — Визначає, чи працює файбер
-   [Fiber::isTerminated](fiber.isterminated.html) — Визначає, чи файбер завершено.
-   [Fiber::suspend](fiber.suspend.html) — Припиняє виконання поточного файбера
-   [Fiber::getCurrent](fiber.getcurrent.html) — Отримує поточний екземпляр Fiber, що виконується.