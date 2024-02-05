---
navigation:
  - swoole-serialize.unpack.md: '« Swoole\\Serialize::unpack'
  - swoole-server.addlistener.md: 'Swoole\\Server::addlistener »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас Swoole\\Server
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Swoole\\Server

(PECL swoole >= 1.9.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class Swoole\Server
     
     {


    /* Методы */
    
   public addlistener(string $host, int $port, string $socket_type): void
public addProcess(swoole_process $process): bool
public after(int $after_time_ms, callable $callback, string $param = ?): ReturnType
public bind(int $fd, int $uid): bool
public clearTimer(int $timer_id): void
swoole_timer_clear(int $timer_id): void
public close(int $fd, bool $reset = ?): bool
public confirm(int $fd): bool
public connection_info(int $fd, int $reactor_id = ?): array
public connection_list(int $start_fd, int $pagesize = ?): array
public defer(callable $callback): void
public Swoole\Server\Port::__destruct(): void
public Swoole\Server\Port::on(string $event_name, callable $callback): ReturnType
public Swoole\Server\Port::set(array $settings): void
public exist(int $fd): bool
public finish(string $data): void
public getClientInfo(int $fd, int $reactor_id = ?, bool $ignore_error = ?): array
public getClientList(int $start_fd, int $pagesize = ?): array
public getLastError(): int
public heartbeat(bool $if_close_connection): mixed
public listen(string $host, int $port, string $socket_type): bool
public on(string $event_name, callable $callback): void
public pause(int $fd): void
public protect(int $fd, bool $is_protected = ?): void
public reload(): bool
public resume(int $fd): void
public send(int $fd, string $data, int $reactor_id = ?): bool
public sendfile(int $fd, string $filename, int $offset = ?): bool
public sendMessage(int $worker_id, string $data): bool
public sendto(    string $ip,    int $port,    string $data,    string $server_socket = ?): bool
public sendwait(int $fd, string $data): bool
public set(array $settings): ReturnType
public shutdown(): void
public start(): void
public stats(): array
public stop(int $worker_id = ?): bool
public task(string $data, int $dst_worker_id = ?, callable $callback = ?): mixed
public taskwait(string $data, float $timeout = ?, int $worker_id = ?): void
public taskWaitMulti(array $tasks, float $timeout_ms = ?): void
public tick(int $interval_ms, callable $callback): void

   }
```

## Зміст

-   [Swoole\\Server::addlistener](swoole-server.addlistener.md)— Додає нового слухача на сервер
-   [Swoole\\Server::addProcess](swoole-server.addprocess.md)— Додає певний користувачем swoole\_process на сервер
-   [Swoole\\Server::after](swoole-server.after.md) \- Запускає callback-функцію після закінчення певного періоду часу
-   [Swoole\\Server::bind](swoole-server.bind.md)— Прив'язує з'єднання до вказаного ідентифікатора користувача
-   [Swoole\\Server::clearTimer](swoole-server.cleartimer.md) \- Зупиняє та знищує таймер
-   [Swoole\\Server::close](swoole-server.close.md) \- Закриває з'єднання з клієнтом
-   [Swoole\\Server::confirm](swoole-server.confirm.md) \- Перевіряє стан з'єднання
-   [Swoole\\Server::connection\_info](swoole-server.connection-info.md)— Отримує інформацію про з'єднання з описом файлу
-   [Swoole\\Server::connection\_list](swoole-server.connection-list.md)— Отримує всі встановлені з'єднання
-   [Swoole\\Server::\_\_construct](swoole-server.construct.md) \- Створює сервер Swoole
-   [Swoole\\Server::defer](swoole-server.defer.md) \- Відкладає виконання callback-функції в кінці поточного EventLoop
-   [Swoole\\Server\\Port::\_\_construct](swoole-server-port.construct.md) \- Створює порт сервера
-   [Swoole\\Server\\Port::\_\_destruct](swoole-server-port.destruct.md)— Знищує порт сервера
-   [Swoole\\Server\\Port::on](swoole-server-port.on.md) \- Реєструє callback-функції події
-   [Swoole\\Server\\Port::set](swoole-server-port.set.md)— Встановлює протокол порту сервера
-   [Swoole\\Server::exist](swoole-server.exist.md)— Перевіряє, чи є з'єднання
-   [Swoole\\Server::finish](swoole-server.finish.md)— Використовується в процесі завдання для надсилання результату до робочого процесу після завершення завдання
-   [Swoole\\Server::getClientInfo](swoole-server.getclientinfo.md)— Отримує інформацію про з'єднання з описом файлу
-   [Swoole\\Server::getClientList](swoole-server.getclientlist.md)— Отримує всі встановлені з'єднання
-   [Swoole\\Server::getLastError](swoole-server.getlasterror.md)— Отримує код останньої помилки
-   [Swoole\\Server::heartbeat](swoole-server.heartbeat.md)— Перевіряє всі з'єднання на сервері
-   [Swoole\\Server::listen](swoole-server.listen.md)— Слухає по заданому IP та порту, тип сокету
-   [Swoole\\Server::on](swoole-server.on.md) \- Реєструє callback-функцію на ім'я події
-   [Swoole\\Server::pause](swoole-server.pause.md)— Припиняє отримання даних від з'єднання
-   [Swoole\\Server::protect](swoole-server.protect.md)— Встановлює з'єднання у захищений режим
-   [Swoole\\Server::reload](swoole-server.reload.md) \- Перезапускає всі робочі процеси
-   [Swoole\\Server::resume](swoole-server.resume.md)— Починає отримувати дані із з'єднання
-   [Swoole\\Server::send](swoole-server.send.md)— Надсилає дані клієнту
-   [Swoole\\Server::sendfile](swoole-server.sendfile.md)— Надсилає файл на з'єднання
-   [Swoole\\Server::sendMessage](swoole-server.sendmessage.md)— Надсилає повідомлення робочим процесам за ідентифікатором
-   [Swoole\\Server::sendto](swoole-server.sendto.md)— Надсилає дані на віддалену UDP-адресу
-   [Swoole\\Server::sendwait](swoole-server.sendwait.md)— Надсилає дані у віддалений сокет блокуючим способом
-   [Swoole\\Server::set](swoole-server.set.md)— Встановлює налаштування часу виконання сервера swoole
-   [Swoole\\Server::shutdown](swoole-server.shutdown.md)— Завершує процес головного сервера, функцію можна викликати у робочих процесах
-   [Swoole\\Server::start](swoole-server.start.md) \- Запускає сервер Swoole
-   [Swoole\\Server::stats](swoole-server.stats.md)— Отримує статистику сервера Swoole
-   [Swoole\\Server::stop](swoole-server.stop.md) \- Зупиняє сервер Swoole
-   [Swoole\\Server::task](swoole-server.task.md)— Надсилає дані до робочих процесів завдання
-   [Swoole\\Server::taskwait](swoole-server.taskwait.md)— Надсилає дані робочим процесам завдання блокуючим способом
-   [Swoole\\Server::taskWaitMulti](swoole-server.taskwaitmulti.md)— Виконує кілька завдань одночасно
-   [Swoole\\Server::tick](swoole-server.tick.md)— Повторює цю функцію у кожний заданий інтервал часу
