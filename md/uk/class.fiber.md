---
navigation:
  - generator.wakeup.md: '« Generator::wakeup'
  - fiber.construct.md: 'Fiber::construct »'
  - index.md: PHP Manual
  - reserved.interfaces.md: Вбудовані інтерфейси та класи
title: Клас Fiber
---
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

[Огляд файберів](language.fibers.md)

## Зміст

-   [Fiber::construct](fiber.construct.md) - Створює новий екземпляр Fiber
-   [Fiber::start](fiber.start.md) - Починає виконання волокна
-   [Fiber::resume](fiber.resume.md) — Відновлює виконання файбера зі значенням
-   [Fiber::throw](fiber.throw.md) — Відновлює виконання файбера за винятком
-   [Fiber::getReturn](fiber.getreturn.md) — Отримує значення, яке повертається файбером
-   [Fiber::isStarted](fiber.isstarted.md) — Визначає, чи запущено файбер
-   [Fiber::isSuspended](fiber.issuspended.md) — Визначає, чи зупинено файбер
-   [Fiber::isRunning](fiber.isrunning.md) — Визначає, чи працює файбер
-   [Fiber::isTerminated](fiber.isterminated.md) — Визначає, чи файбер завершено.
-   [Fiber::suspend](fiber.suspend.md) — Припиняє виконання поточного файбера
-   [Fiber::getCurrent](fiber.getcurrent.md) — Отримує поточний екземпляр Fiber, що виконується.
