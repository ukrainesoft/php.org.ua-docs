---
navigation:
  - gearmanjob.workloadsize.md: '« GearmanJob::workloadSize'
  - gearmantask.construct.md: 'GearmanTask::\_\_construct »'
  - index.md: PHP Manual
  - book.gearman.md: Gearman
title: Клас GearmanTask
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

    public data(): false|string
public dataSize(): int|false
public functionName(): false|string
public isKnown(): bool
public isRunning(): bool
public jobHandle(): false|string
public recvData(int $data_len): false|array
public returnCode(): int
public sendWorkload(string $data): int|false
public taskDenominator(): false|int
public taskNumerator(): false|int
public unique(): false|string

   }
```

## Зміст

-   [GearmanTask::\_\_construct](gearmantask.construct.md)— Створює об'єкт GearmanTask
-   [GearmanTask::create](gearmantask.create.md) \- Створює завдання (застарілий метод)
-   [GearmanTask::data](gearmantask.data.md)— Отримати дані, повернені до завдання
-   [GearmanTask::dataSize](gearmantask.datasize.md)— Отримати розмір даних, що повертаються
-   [GearmanTask::function](gearmantask.function.md)— Отримати ім'я пов'язаної функції (застарілий метод)
-   [GearmanTask::functionName](gearmantask.functionname.md)— Отримати ім'я функції
-   [GearmanTask::isKnown](gearmantask.isknown.md)— Визначення, чи відомо серверу про це завдання
-   [GearmanTask::isRunning](gearmantask.isrunning.md)— Перевіряє, чи виконується завдання на даний момент
-   [GearmanTask::jobHandle](gearmantask.jobhandle.md)— Отримати дескриптор завдання
-   [GearmanTask::recvData](gearmantask.recvdata.md)— Читання даних роботи чи результату завдання у буфер
-   [GearmanTask::returnCode](gearmantask.returncode.md)— Отримати останній код повернення
-   [GearmanTask::sendData](gearmantask.senddata.md)— Надсилання даних завдання (застарілий метод)
-   [GearmanTask::sendWorkload](gearmantask.sendworkload.md)— Надсилання даних завдання
-   [GearmanTask::taskDenominator](gearmantask.taskdenominator.md)— Отримати знаменник відсотка виконаної роботи
-   [GearmanTask::taskNumerator](gearmantask.tasknumerator.md)— Отримання чисельника відсотка виконаної роботи
-   [GearmanTask::unique](gearmantask.unique.md)— Отримання унікального ідентифікатора завдання
-   [GearmanTask::uuid](gearmantask.uuid.md) \- Отримання унікального ідентифікатора завдання (застарілий метод)
