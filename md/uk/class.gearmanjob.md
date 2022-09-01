---
navigation:
  - gearmanclient.wait.html: '« GearmanClient::wait'
  - gearmanjob.complete.html: 'GearmanJob::complete »'
  - index.html: PHP Manual
  - book.gearman.html: Gearman
title: Клас GearmanJob
---
# Клас GearmanJob

(PECL gearman >= 0.5.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class GearmanJob
     
     {


    /* Методы */
    
   public complete(string $result): bool
public __construct()
public data(string $data): bool
public exception(string $exception): bool
public fail(): bool
public functionName(): string
public handle(): string
public returnCode(): int
public sendComplete(string $result): bool
public sendData(string $data): bool
public sendException(string $exception): bool
public sendFail(): bool
public sendStatus(int $numerator, int $denominator): bool
public sendWarning(string $warning): bool
public setReturn(int $gearman_return_t): bool
public status(int $numerator, int $denominator): bool
public unique(): string
public warning(string $warning): bool
public workload(): string
public workloadSize(): int

   }
```

## Зміст

-   [GearmanJob::complete](gearmanjob.complete.html) — Надсилання результату та статусу завершення (застарілий метод)
-   [GearmanJob::construct](gearmanjob.construct.html) - Створення об'єкта GearmanJob
-   [GearmanJob::data](gearmanjob.data.html) — Надсилання даних (застарілий метод)
-   [GearmanJob::exception](gearmanjob.exception.html) — Надсилання виключення (застарілий метод)
-   [GearmanJob::fail](gearmanjob.fail.html) — Надсилання статусу невдалої операції (застарілий метод)
-   [GearmanJob::functionName](gearmanjob.functionname.html) — Отримання імені функції
-   [GearmanJob::handle](gearmanjob.handle.html) — Отримання дескриптора об'єкта завдання
-   [GearmanJob::returnCode](gearmanjob.returncode.html) — Отримання останнього коду повернення
-   [GearmanJob::sendComplete](gearmanjob.sendcomplete.html) — Надсилання результату та статусу завершення
-   [GearmanJob::sendData](gearmanjob.senddata.html) — Відправлення даних завдання, що виконується
-   [GearmanJob::sendException](gearmanjob.sendexception.html) — Відправлення виключення завдання, що виконується.
-   [GearmanJob::sendFail](gearmanjob.sendfail.html) — Надсилання статусу невдалої операції
-   [GearmanJob::sendStatus](gearmanjob.sendstatus.html) — Надсилання статусу
-   [GearmanJob::sendWarning](gearmanjob.sendwarning.html) — Надсилання попередження
-   [GearmanJob::setReturn](gearmanjob.setreturn.html) — Встановлення значення, що повертається
-   [GearmanJob::status](gearmanjob.status.html) — Надсилання статусу завдання (застарілий метод)
-   [GearmanJob::unique](gearmanjob.unique.html) — Отримання унікального ідентифікатора
-   [GearmanJob::warning](gearmanjob.warning.html) — Надсилання попередження (застарілий метод)
-   [GearmanJob::workload](gearmanjob.workload.html) — Отримання даних для обробки
-   [GearmanJob::workloadSize](gearmanjob.workloadsize.html) — Отримання розміру даних, що обробляються
