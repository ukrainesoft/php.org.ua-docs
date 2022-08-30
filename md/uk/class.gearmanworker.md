Клас GearmanWorker

-   [« GearmanTask::uuid](gearmantask.uuid.html)
    
-   [GearmanWorker::addFunction »](gearmanworker.addfunction.html)
    
-   [PHP Manual](index.html)
    
-   [Gearman](book.gearman.html)
    
-   Клас GearmanWorker
    

# Клас GearmanWorker

(PECL gearman >= 0.5.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class GearmanWorker
     
     {


    /* Методы */
    
   public addFunction(    string $function_name,    callable $function,    mixed &$context = ?,    int $timeout = ?): bool
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

-   [GearmanWorker::addFunction](gearmanworker.addfunction.html) — Реєстрація та додавання callback-функції
-   [GearmanWorker::addOptions](gearmanworker.addoptions.html) — Додавання налаштувань обробника
-   [GearmanWorker::addServer](gearmanworker.addserver.html) — Додавання сервера завдань
-   [GearmanWorker::addServers](gearmanworker.addservers.html) — Додавання серверів завдань
-   [GearmanWorker::clone](gearmanworker.clone.html) - Створення копії оброблювача
-   [GearmanWorker::construct](gearmanworker.construct.html) - Створення об'єкта GearmanWorker
-   [GearmanWorker::echo](gearmanworker.echo.html) - Перевірка відгуку серверів завдань
-   [GearmanWorker::error](gearmanworker.error.html) — Отримання останньої виявленої помилки
-   [GearmanWorker::getErrno](gearmanworker.geterrno.html) — Отримання номера помилки
-   [GearmanWorker::options](gearmanworker.options.html) — Отримання налаштувань обробника
-   [GearmanWorker::register](gearmanworker.register.html) - Реєстрація функції на сервері завдань
-   [GearmanWorker::removeOptions](gearmanworker.removeoptions.html) — Видалення налаштувань обробника
-   [GearmanWorker::returnCode](gearmanworker.returncode.html) - Отримання останнього коду повернення Gearman
-   [GearmanWorker::setId](gearmanworker.setid.html) — Призначає обробнику ідентифікатор, щоб надалі мати можливість опитати всі доступні обробники
-   [GearmanWorker::setOptions](gearmanworker.setoptions.html) — Встановлення налаштувань обробника
-   [GearmanWorker::setTimeout](gearmanworker.settimeout.html) — Завдання часу очікування на введення/виведення на сокеті
-   [GearmanWorker::timeout](gearmanworker.timeout.html) — Отримання значення час очікування запитів на сокеті
-   [GearmanWorker::unregister](gearmanworker.unregister.html) — Видалити реєстрацію імені функції на всіх серверах завдань
-   [GearmanWorker::unregisterAll](gearmanworker.unregisterall.html) — Видалення реєстрації всіх імен функцій на серверах завдань
-   [GearmanWorker::wait](gearmanworker.wait.html) — Очікування запиту з одного із серверів завдань
-   [GearmanWorker::work](gearmanworker.work.html) — Очікування та виконання завдань