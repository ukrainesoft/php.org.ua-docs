---
navigation:
  - gearmanjob.workloadsize.md: '« GearmanJob::workloadSize'
  - gearmantask.construct.md: 'GearmanTask::construct »'
  - index.md: PHP Manual
  - book.gearman.md: Gearman
title: Клас GearmanTask
---
# Клас GearmanTask

(PECL gearman >= 0.5.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class GearmanTask
     
     {


    /* Методы */
    
   public __construct()
public create(): GearmanTask|false
public data(): string
public dataSize(): int
public function(): string
public functionName(): string
public isKnown(): bool
public isRunning(): bool
public jobHandle(): string
public recvData(int $data_len): array
public returnCode(): int
public sendData(string $data): int
public sendWorkload(string $data): int
public taskDenominator(): int
public taskNumerator(): int
public unique(): string
public uuid(): string

   }
```

## Зміст

-   [GearmanTask::construct](gearmantask.construct.md) — Створює об'єкт GearmanTask
-   [GearmanTask::create](gearmantask.create.md) - Створює завдання (застарілий метод)
-   [GearmanTask::data](gearmantask.data.md) — Отримати дані, повернені до завдання
-   [GearmanTask::dataSize](gearmantask.datasize.md) — Отримати розмір даних, що повертаються
-   [GearmanTask::function](gearmantask.function.md) — Отримати ім'я пов'язаної функції (застарілий метод)
-   [GearmanTask::functionName](gearmantask.functionname.md) — Отримати ім'я функції
-   [GearmanTask::isKnown](gearmantask.isknown.md) — Визначення, чи відомо серверу про це завдання
-   [GearmanTask::isRunning](gearmantask.isrunning.md) — Перевіряє, чи виконується завдання на даний момент
-   [GearmanTask::jobHandle](gearmantask.jobhandle.md) — Отримати дескриптор завдання
-   [GearmanTask::recvData](gearmantask.recvdata.md) — Читання даних роботи чи результату завдання у буфер
-   [GearmanTask::returnCode](gearmantask.returncode.md) — Отримати останній код повернення
-   [GearmanTask::sendData](gearmantask.senddata.md) — Надсилання даних завдання (застарілий метод)
-   [GearmanTask::sendWorkload](gearmantask.sendworkload.md) — Надсилання даних завдання
-   [GearmanTask::taskDenominator](gearmantask.taskdenominator.md) — Отримати знаменник відсотка виконаної роботи
-   [GearmanTask::taskNumerator](gearmantask.tasknumerator.md) — Отримання чисельника відсотка виконаної роботи
-   [GearmanTask::unique](gearmantask.unique.md) — Отримання унікального ідентифікатора завдання
-   [GearmanTask::uuid](gearmantask.uuid.md) - Отримання унікального ідентифікатора завдання (застарілий метод)
