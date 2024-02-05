---
navigation:
  - gearman.examples-reverse-task.md: '« Базові клієнт та обробник Gearman, відправка завдань'
  - gearmanclient.addoptions.md: 'GearmanClient::addOptions »'
  - index.md: PHP Manual
  - book.gearman.md: Gearman
title: Клас GearmanClient
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас GearmanClient

(PECL gearman >= 0.5.0)

## Вступ

Це клас для підключення до сервера завдань Gearman і створення запитів для виконання певної функції за наданими даними. Функція, що виконується, повинна бути зареєстрована обробником (worker) Gearman і передані дані є непрозорими для сервера завдань.

## Огляд класів

```classsynopsis

    
     class GearmanClient
     {

    /* Методы */
    
   public __construct()

    public addOptions(int $option): bool
public addServer(string $host = null, int $port = 0, bool $setupExceptionHandler = true): bool
public addServers(string $servers = null, bool $setupExceptionHandler = true): bool
public addTask(    string $function_name,    string|int|float $workload,    mixed $context = null,    ?string $unique_key = null): GearmanTask|false
public addTaskBackground(    string $function_name,    string|int|float $workload,    mixed $context = null,    ?string $unique_key = null): GearmanTask|false
public addTaskHigh(    string $function_name,    string|int|float $workload,    mixed $context = null,    ?string $unique_key = null): GearmanTask|false
public addTaskHighBackground(    string $function_name,    string|int|float $workload,    mixed $context = null,    ?string $unique_key = null): GearmanTask|false
public addTaskLow(    string $function_name,    string|int|float $workload,    mixed $context = null,    ?string $unique_key = null): GearmanTask|false
public addTaskLowBackground(    string $function_name,    string|int|float $workload,    mixed $context = null,    ?string $unique_key = null): GearmanTask|false
public addTaskStatus(string $job_handle, mixed $context = null): GearmanTask|false
public clearCallbacks(): bool
public context(): string
public doBackground(string $function, string $workload, ?string $unique = null): string
public doHigh(string $function, string $workload, ?string $unique = null): string
public doHighBackground(string $function, string $workload, ?string $unique = null): string
public doJobHandle(): string
public doLow(string $function, string $workload, ?string $unique = null): string
public doLowBackground(string $function, string $workload, ?string $unique = null): string
public doNormal(string $function, string $workload, ?string $unique = null): string
public doStatus(): array
public error(): string|false
public getErrno(): int
public jobStatus(string $job_handle): array
public ping(string $workload): bool
public removeOptions(int $option): bool
public returnCode(): int
public runTasks(): bool
public setCompleteCallback(callable $function): bool
public setContext(string $data): bool
public setCreatedCallback(callable $function): bool
public setDataCallback(callable $function): bool
public setExceptionCallback(callable $function): bool
public setFailCallback(callable $function): bool
public setOptions(int $option): bool
public setStatusCallback(callable $function): bool
public setTimeout(int $timeout): bool
public setWarningCallback(callable $function): bool
public setWorkloadCallback(callable $function): bool
public timeout(): int
public wait(): bool

   }
```

## Зміст

-   [GearmanClient::addOptions](gearmanclient.addoptions.md) \- Додати клієнтські опції
-   [GearmanClient::addServer](gearmanclient.addserver.md) \- Додати сервер завдань для клієнта
-   [GearmanClient::addServers](gearmanclient.addservers.md) \- Додати список серверів завдань для клієнта
-   [GearmanClient::addTask](gearmanclient.addtask.md)— Додати завдання, яке буде виконано у паралельному режимі
-   [GearmanClient::addTaskBackground](gearmanclient.addtaskbackground.md)— Додати фонове завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskHigh](gearmanclient.addtaskhigh.md)— Додати високопріоритетне завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskHighBackground](gearmanclient.addtaskhighbackground.md)— Додати високопріоритетне фонове завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskLow](gearmanclient.addtasklow.md)— Додати низькопріоритетне завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskLowBackground](gearmanclient.addtasklowbackground.md)— Додати низькопріоритетне фонове завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskStatus](gearmanclient.addtaskstatus.md)— Додати завдання для набуття статусу
-   [GearmanClient::clearCallbacks](gearmanclient.clearcallbacks.md)— Очистити всі функції зворотного виклику цієї задачі
-   [GearmanClient::clone](gearmanclient.clone.md) \- Створити копію об'єкта GearmanClient
-   [GearmanClient::\_\_construct](gearmanclient.construct.md) \- Створити екземпляр GearmanClient
-   [GearmanClient::context](gearmanclient.context.md)— Повертає контекст програми
-   [GearmanClient::data](gearmanclient.data.md)— Повертає дані програми (функція застаріла)
-   [GearmanClient::do](gearmanclient.do.md)— Виконує одне завдання та повертає результат\[Застарілий метод\]
-   [GearmanClient::doBackground](gearmanclient.dobackground.md)— Запуск виконання завдання у фоновому режимі
-   [GearmanClient::doHigh](gearmanclient.dohigh.md)— Запускає на виконання завдання із високим пріоритетом
-   [GearmanClient::doHighBackground](gearmanclient.dohighbackground.md)— Запускає на виконання із високим пріоритетом завдання у фоновому режимі
-   [GearmanClient::doJobHandle](gearmanclient.dojobhandle.md)— Отримати дескриптор завдання, що виконується
-   [GearmanClient::doLow](gearmanclient.dolow.md)— Запускає на виконання завдання із низьким пріоритетом
-   [GearmanClient::doLowBackground](gearmanclient.dolowbackground.md)— Запускає на виконання з низьким пріоритетом завдання у фоновому режимі
-   [GearmanClient::doNormal](gearmanclient.donormal.md)— Виконує одиночне завдання та повертає результат
-   [GearmanClient::doStatus](gearmanclient.dostatus.md)— Отримання статусу завдання, що виконується
-   [GearmanClient::echo](gearmanclient.echo.md)— Надсилає дані всім серверам завдань, щоб перевірити відгук\[Застарілий метод\]
-   [GearmanClient::error](gearmanclient.error.md)— Повернути рядок помилки для останньої виявленої помилки
-   [GearmanClient::getErrno](gearmanclient.geterrno.md)— Отримати значення errno
-   [GearmanClient::jobStatus](gearmanclient.jobstatus.md)— Набуття статусу виконання фонового завдання
-   [GearmanClient::ping](gearmanclient.ping.md)— Надсилає дані на всі сервери, щоб перевірити, які з них виведуть ці дані
-   [GearmanClient::removeOptions](gearmanclient.removeoptions.md)— Видалити опції клієнта
-   [GearmanClient::returnCode](gearmanclient.returncode.md) \- Отримати останній код повернення Gearman
-   [GearmanClient::runTasks](gearmanclient.runtasks.md)— Запустити список завдань у паралельному режимі
-   [GearmanClient::setClientCallback](gearmanclient.setclientcallback.md)— Встановити функцію зворотного дзвінка, коли є пакет даних для завдання (застарілий метод)
-   [GearmanClient::setCompleteCallback](gearmanclient.setcompletecallback.md)— Встановіть функцію, яка буде викликана після завершення завдання
-   [GearmanClient::setContext](gearmanclient.setcontext.md)— Встановити контекст програми
-   [GearmanClient::setCreatedCallback](gearmanclient.setcreatedcallback.md)— Встановити функцію зворотного дзвінка, коли завдання ставиться в чергу
-   [GearmanClient::setData](gearmanclient.setdata.md)— Встановити дані програми (застарілий метод)
-   [GearmanClient::setDataCallback](gearmanclient.setdatacallback.md) \- Задає callback-функцію для обробки переданих даних
-   [GearmanClient::setExceptionCallback](gearmanclient.setexceptioncallback.md)— Встановити функцію зворотного виклику для перехоплення виключень обробника завдань
-   [GearmanClient::setFailCallback](gearmanclient.setfailcallback.md)— Встановити callback-функцію для обробки ситуації, коли завдання не вдалося виконати
-   [GearmanClient::setOptions](gearmanclient.setoptions.md)— Встановлення налаштувань клієнта
-   [GearmanClient::setStatusCallback](gearmanclient.setstatuscallback.md) \- Завдання callback-функції, що збирає інформацію про стан обробника завдань
-   [GearmanClient::setTimeout](gearmanclient.settimeout.md)— Встановлення часу очікування для введення/виводу.
-   [GearmanClient::setWarningCallback](gearmanclient.setwarningcallback.md)— Установка callback-функції, яка обслуговує попередження оброблювача завдань
-   [GearmanClient::setWorkloadCallback](gearmanclient.setworkloadcallback.md) \- Установка callback-функції, що приймає проміжні результати від оброблювача завдань
-   [GearmanClient::timeout](gearmanclient.timeout.md)— Отримання часу очікування операцій введення/виводу
-   [GearmanClient::wait](gearmanclient.wait.md)— Чекає на активність введення-виводу для всіх підключень на клієнті
