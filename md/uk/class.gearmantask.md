Клас GearmanTask

-   [« GearmanJob::workloadSize](gearmanjob.workloadsize.html)
    
-   [GearmanTask::\_\_construct »](gearmantask.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Gearman](book.gearman.html)
    
-   Клас GearmanTask
    

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

-   [GearmanTask::\_\_construct](gearmantask.construct.html) — Створює об'єкт GearmanTask
-   [GearmanTask::create](gearmantask.create.html) - Створює завдання (застарілий метод)
-   [GearmanTask::data](gearmantask.data.html) — Отримати дані, повернені до завдання
-   [GearmanTask::dataSize](gearmantask.datasize.html) — Отримати розмір даних, що повертаються
-   [GearmanTask::function](gearmantask.function.html) — Отримати ім'я пов'язаної функції (застарілий метод)
-   [GearmanTask::functionName](gearmantask.functionname.html) — Отримати ім'я функції
-   [GearmanTask::isKnown](gearmantask.isknown.html) — Визначення, чи відомо серверу про це завдання
-   [GearmanTask::isRunning](gearmantask.isrunning.html) — Перевіряє, чи виконується завдання на даний момент
-   [GearmanTask::jobHandle](gearmantask.jobhandle.html) — Отримати дескриптор завдання
-   [GearmanTask::recvData](gearmantask.recvdata.html) — Читання даних роботи чи результату завдання у буфер
-   [GearmanTask::returnCode](gearmantask.returncode.html) — Отримати останній код повернення
-   [GearmanTask::sendData](gearmantask.senddata.html) — Надсилання даних завдання (застарілий метод)
-   [GearmanTask::sendWorkload](gearmantask.sendworkload.html) — Надсилання даних завдання
-   [GearmanTask::taskDenominator](gearmantask.taskdenominator.html) — Отримати знаменник відсотка виконаної роботи
-   [GearmanTask::taskNumerator](gearmantask.tasknumerator.html) — Отримання чисельника відсотка виконаної роботи
-   [GearmanTask::unique](gearmantask.unique.html) — Отримання унікального ідентифікатора завдання
-   [GearmanTask::uuid](gearmantask.uuid.html) - Отримання унікального ідентифікатора завдання (застарілий метод)