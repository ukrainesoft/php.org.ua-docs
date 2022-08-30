Клас GearmanClient

-   [« Базовые клиент и обработчик Gearman, отправка задач](gearman.examples-reverse-task.html)
    
-   [GearmanClient::addOptions »](gearmanclient.addoptions.html)
    
-   [PHP Manual](index.html)
    
-   [Gearman](book.gearman.html)
    
-   Клас GearmanClient
    

# Клас GearmanClient

(PECL gearman >= 0.5.0)

## Вступ

Це клас для підключення до сервера завдань Gearman і створення запитів для виконання певної функції за наданими даними. Функція, що виконується, повинна бути зареєстрована обробником (worker) Gearman і передані дані є непрозорими для сервера завдань.

## Огляд класів

```classsynopsis



    
     
      class GearmanClient
     
     {


    /* Методы */
    
   public addOptions(int $options): bool
public addServer(string $host = 127.0.0.1, int $port = 4730): bool
public addServers(string $servers = 127.0.0.1:4730): bool
public addTask(    string $function_name,    string $workload,    mixed &$context = ?,    string $unique = ?): GearmanTask
public addTaskBackground(    string $function_name,    string $workload,    mixed &$context = ?,    string $unique = ?): GearmanTask
public addTaskHigh(    string $function_name,    string $workload,    mixed &$context = ?,    string $unique = ?): GearmanTask
public addTaskHighBackground(    string $function_name,    string $workload,    mixed &$context = ?,    string $unique = ?): GearmanTask
public addTaskLow(    string $function_name,    string $workload,    mixed &$context = ?,    string $unique = ?): GearmanTask
public addTaskLowBackground(    string $function_name,    string $workload,    mixed &$context = ?,    string $unique = ?): GearmanTask
public addTaskStatus(string $job_handle, string &$context = ?): GearmanTask
public clearCallbacks(): bool
public clone(): GearmanClient
public __construct()
public context(): string
public data(): string
public do(string $function_name, string $workload, string $unique = ?): string
public doBackground(string $function_name, string $workload, string $unique = ?): string
public doHigh(string $function_name, string $workload, string $unique = ?): string
public doHighBackground(string $function_name, string $workload, string $unique = ?): string
public doJobHandle(): string
public doLow(string $function_name, string $workload, string $unique = ?): string
public doLowBackground(string $function_name, string $workload, string $unique = ?): string
public doNormal(string $function_name, string $workload, string $unique = ?): string
public doStatus(): array
public echo(string $workload): bool
public error(): string
public getErrno(): int
public jobStatus(string $job_handle): array
public ping(string $workload): bool
public removeOptions(int $options): bool
public returnCode(): int
public runTasks(): bool
public setClientCallback(callable $callback): void
public setCompleteCallback(callable $callback): bool
public setContext(string $context): bool
public setCreatedCallback(string $callback): bool
public setData(string $data): bool
public setDataCallback(callable $callback): bool
public setExceptionCallback(callable $callback): bool
public setFailCallback(callable $callback): bool
public setOptions(int $options): bool
public setStatusCallback(callable $callback): bool
public setTimeout(int $timeout): bool
public setWarningCallback(callable $callback): bool
public setWorkloadCallback(callable $callback): bool
public timeout(): int
public wait(): bool

   }
```

## Зміст

-   [GearmanClient::addOptions](gearmanclient.addoptions.html) - Додати клієнтські опції
-   [GearmanClient::addServer](gearmanclient.addserver.html) - Додати сервер завдань для клієнта
-   [GearmanClient::addServers](gearmanclient.addservers.html) - Додати список серверів завдань для клієнта
-   [GearmanClient::addTask](gearmanclient.addtask.html) — Додати завдання, яке буде виконано у паралельному режимі
-   [GearmanClient::addTaskBackground](gearmanclient.addtaskbackground.html) — Додати фонове завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskHigh](gearmanclient.addtaskhigh.html) — Додати високопріоритетне завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskHighBackground](gearmanclient.addtaskhighbackground.html) — Додати високопріоритетне фонове завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskLow](gearmanclient.addtasklow.html) — Додати низькопріоритетне завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskLowBackground](gearmanclient.addtasklowbackground.html) — Додати низькопріоритетне фонове завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskStatus](gearmanclient.addtaskstatus.html) — Додати завдання для набуття статусу
-   [GearmanClient::clearCallbacks](gearmanclient.clearcallbacks.html) — Очистити всі функції зворотного виклику цієї задачі
-   [GearmanClient::clone](gearmanclient.clone.html) - Створити копію об'єкта GearmanClient
-   [GearmanClient::construct](gearmanclient.construct.html) - Створити екземпляр GearmanClient
-   [GearmanClient::context](gearmanclient.context.html) — Повертає контекст програми
-   [GearmanClient::data](gearmanclient.data.html) — Повертає дані програми (функція застаріла)
-   [GearmanClient::do](gearmanclient.do.html) — Виконує одне завдання та повертає результат Застарілий метод
-   [GearmanClient::doBackground](gearmanclient.dobackground.html) — Запуск виконання завдання у фоновому режимі
-   [GearmanClient::doHigh](gearmanclient.dohigh.html) — Запускає на виконання завдання із високим пріоритетом
-   [GearmanClient::doHighBackground](gearmanclient.dohighbackground.html) — Запускає на виконання із високим пріоритетом завдання у фоновому режимі
-   [GearmanClient::doJobHandle](gearmanclient.dojobhandle.html) — Отримати дескриптор завдання, що виконується
-   [GearmanClient::doLow](gearmanclient.dolow.html) — Запускає на виконання завдання із низьким пріоритетом
-   [GearmanClient::doLowBackground](gearmanclient.dolowbackground.html) — Запускає на виконання з низьким пріоритетом завдання у фоновому режимі
-   [GearmanClient::doNormal](gearmanclient.donormal.html) — Виконує одиночне завдання та повертає результат
-   [GearmanClient::doStatus](gearmanclient.dostatus.html) — Отримання статусу завдання, що виконується
-   [GearmanClient::echo](gearmanclient.echo.html) — Надсилає дані всім серверам завдань, щоб перевірити відгук Застарілий метод
-   [GearmanClient::error](gearmanclient.error.html) — Повернути рядок помилки для останньої виявленої помилки
-   [GearmanClient::getErrno](gearmanclient.geterrno.html) — Отримати значення errno
-   [GearmanClient::jobStatus](gearmanclient.jobstatus.html) — Набуття статусу виконання фонового завдання
-   [GearmanClient::ping](gearmanclient.ping.html) — Надсилає дані на всі сервери, щоб перевірити, які з них виведуть ці дані
-   [GearmanClient::removeOptions](gearmanclient.removeoptions.html) — Видалити опції клієнта
-   [GearmanClient::returnCode](gearmanclient.returncode.html) - Отримати останній код повернення Gearman
-   [GearmanClient::runTasks](gearmanclient.runtasks.html) — Запустити список завдань у паралельному режимі
-   [GearmanClient::setClientCallback](gearmanclient.setclientcallback.html) — Встановити функцію зворотного дзвінка, коли є пакет даних для завдання (застарілий метод)
-   [GearmanClient::setCompleteCallback](gearmanclient.setcompletecallback.html) — Встановіть функцію, яка буде викликана після завершення завдання
-   [GearmanClient::setContext](gearmanclient.setcontext.html) — Встановити контекст програми
-   [GearmanClient::setCreatedCallback](gearmanclient.setcreatedcallback.html) — Встановити функцію зворотного дзвінка, коли завдання ставиться в чергу
-   [GearmanClient::setData](gearmanclient.setdata.html) — Встановити дані програми (застарілий метод)
-   [GearmanClient::setDataCallback](gearmanclient.setdatacallback.html) - Задає callback-функцію для обробки переданих даних
-   [GearmanClient::setExceptionCallback](gearmanclient.setexceptioncallback.html) — Встановити функцію зворотного виклику для перехоплення виключень обробника завдань
-   [GearmanClient::setFailCallback](gearmanclient.setfailcallback.html) — Встановити callback-функцію для обробки ситуації, коли завдання не вдалося виконати
-   [GearmanClient::setOptions](gearmanclient.setoptions.html) — Встановлення налаштувань клієнта
-   [GearmanClient::setStatusCallback](gearmanclient.setstatuscallback.html) - Завдання callback-функції, що збирає інформацію про стан обробника завдань
-   [GearmanClient::setTimeout](gearmanclient.settimeout.html) — Встановлення часу очікування для введення/виводу.
-   [GearmanClient::setWarningCallback](gearmanclient.setwarningcallback.html) - Установка callback-функції, що обслуговує попередження оброблювача завдань
-   [GearmanClient::setWorkloadCallback](gearmanclient.setworkloadcallback.html) - Установка callback-функції, що приймає проміжні результати від оброблювача завдань
-   [GearmanClient::timeout](gearmanclient.timeout.html) — Отримання часу очікування операцій введення/виводу
-   [GearmanClient::wait](gearmanclient.wait.html) — Чекає на активність введення-виводу для всіх підключень на клієнті