---
navigation:
  - gearmanclient.wait.md: '« GearmanClient::wait'
  - gearmanjob.complete.md: 'GearmanJob::complete »'
  - index.md: PHP Manual
  - book.gearman.md: Gearman
title: Клас GearmanJob
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас GearmanJob

(PECL gearman >= 0.5.0)

## Вступ

## Огляд класів

```classsynopsis

    
     class GearmanJob
     {

    /* Методы */
    
   public functionName(): false|string
public handle(): false|string
public returnCode(): int
public sendComplete(string $result): bool
public sendData(string $data): bool
public sendException(string $exception): bool
public sendFail(): bool
public sendStatus(int $numerator, int $denominator): bool
public sendWarning(string $warning): bool
public setReturn(int $gearman_return_t): bool
public unique(): false|string
public workload(): string
public workloadSize(): int

   }
```

## Зміст

-   [GearmanJob::complete](gearmanjob.complete.md)— Надсилання результату та статусу завершення (застарілий метод)
-   [GearmanJob::\_\_construct](gearmanjob.construct.md)— Створення об'єкту GearmanJob
-   [GearmanJob::data](gearmanjob.data.md)— Надсилання даних (застарілий метод)
-   [GearmanJob::exception](gearmanjob.exception.md)— Надсилання виключення (застарілий метод)
-   [GearmanJob::fail](gearmanjob.fail.md)— Надсилання статусу невдалої операції (застарілий метод)
-   [GearmanJob::functionName](gearmanjob.functionname.md)— Отримання імені функції
-   [GearmanJob::handle](gearmanjob.handle.md)— Отримання дескриптора об'єкта завдання
-   [GearmanJob::returnCode](gearmanjob.returncode.md)— Отримання останнього коду повернення
-   [GearmanJob::sendComplete](gearmanjob.sendcomplete.md)— Надсилання результату та статусу завершення
-   [GearmanJob::sendData](gearmanjob.senddata.md)— Відправлення даних завдання, що виконується
-   [GearmanJob::sendException](gearmanjob.sendexception.md)— Відправлення виключення завдання, що виконується.
-   [GearmanJob::sendFail](gearmanjob.sendfail.md)— Надсилання статусу невдалої операції
-   [GearmanJob::sendStatus](gearmanjob.sendstatus.md)— Надсилання статусу
-   [GearmanJob::sendWarning](gearmanjob.sendwarning.md)— Надсилання попередження
-   [GearmanJob::setReturn](gearmanjob.setreturn.md)— Встановлення значення, що повертається
-   [GearmanJob::status](gearmanjob.status.md)— Надсилання статусу завдання (застарілий метод)
-   [GearmanJob::unique](gearmanjob.unique.md)— Отримання унікального ідентифікатора
-   [GearmanJob::warning](gearmanjob.warning.md)— Надсилання попередження (застарілий метод)
-   [GearmanJob::workload](gearmanjob.workload.md)— Отримання даних для обробки
-   [GearmanJob::workloadSize](gearmanjob.workloadsize.md)— Отримання розміру даних, що обробляються
