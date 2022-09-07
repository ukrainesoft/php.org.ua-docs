---
navigation:
  - gearmantask.uuid.md: '« GearmanTask::uuid'
  - gearmanworker.addfunction.md: 'GearmanWorker::addFunction »'
  - index.md: PHP Manual
  - book.gearman.md: Gearman
title: Клас GearmanWorker
---
# Клас GearmanWorker

(PECL gearman >= 0.5.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class GearmanWorker
     
     {


    /* Методы */
    
   public addFunction(    string $function_name,    callable $function,    mixed &$context = ?,    int $timeout = ?): bool
public addOptions(int $option): bool
public addServer(string $host = 127.0.0.1, int $port = 4730): bool
public addServers(string $servers = 127.0.0.1:4730): bool
public clone(): void
public __construct()
public echo(string $workload): bool
public error(): string
public getErrno(): int
public options(): int
public register(string $function_name, int $timeout = ?): bool
public removeOptions(int $option): bool
public returnCode(): int
public setId(string $id): bool
public setOptions(int $option): bool
public setTimeout(int $timeout): bool
public timeout(): int
public unregister(string $function_name): bool
public unregisterAll(): bool
public wait(): bool
public work(): bool

   }
```

## Зміст

-   [GearmanWorker::addFunction](gearmanworker.addfunction.md) — Реєстрація та додавання callback-функції
-   [GearmanWorker::addOptions](gearmanworker.addoptions.md) — Додавання налаштувань обробника
-   [GearmanWorker::addServer](gearmanworker.addserver.md) — Додавання сервера завдань
-   [GearmanWorker::addServers](gearmanworker.addservers.md) — Додавання серверів завдань
-   [GearmanWorker::clone](gearmanworker.clone.md) - Створення копії оброблювача
-   [GearmanWorker::construct](gearmanworker.construct.md) - Створення об'єкта GearmanWorker
-   [GearmanWorker::echo](gearmanworker.echo.md) - Перевірка відгуку серверів завдань
-   [GearmanWorker::error](gearmanworker.error.md) — Отримання останньої виявленої помилки
-   [GearmanWorker::getErrno](gearmanworker.geterrno.md) — Отримання номера помилки
-   [GearmanWorker::options](gearmanworker.options.md) — Отримання налаштувань обробника
-   [GearmanWorker::register](gearmanworker.register.md) - Реєстрація функції на сервері завдань
-   [GearmanWorker::removeOptions](gearmanworker.removeoptions.md) — Видалення налаштувань обробника
-   [GearmanWorker::returnCode](gearmanworker.returncode.md) - Отримання останнього коду повернення Gearman
-   [GearmanWorker::setId](gearmanworker.setid.md) — Призначає обробнику ідентифікатор, щоб надалі мати можливість опитати всі доступні обробники
-   [GearmanWorker::setOptions](gearmanworker.setoptions.md) — Встановлення налаштувань обробника
-   [GearmanWorker::setTimeout](gearmanworker.settimeout.md) — Завдання часу очікування на введення/виведення на сокеті
-   [GearmanWorker::timeout](gearmanworker.timeout.md) — Отримання значення час очікування запитів на сокеті
-   [GearmanWorker::unregister](gearmanworker.unregister.md) — Видалити реєстрацію імені функції на всіх серверах завдань
-   [GearmanWorker::unregisterAll](gearmanworker.unregisterall.md) — Видалення реєстрації всіх імен функцій на серверах завдань
-   [GearmanWorker::wait](gearmanworker.wait.md) — Очікування запиту з одного із серверів завдань
-   [GearmanWorker::work](gearmanworker.work.md) — Очікування та виконання завдань
