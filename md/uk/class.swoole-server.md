Клас SwooleServer

-   [« SwooleSerialize::unpack](swoole-serialize.unpack.html)
    
-   [SwooleServer::addlistener »](swoole-server.addlistener.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole](book.swoole.html)
    
-   Клас SwooleServer
    

# Клас SwooleServer

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
public taskWaitMulti(array $tasks, double $timeout_ms = ?): void
public tick(int $interval_ms, callable $callback): void

   }
```

## Зміст

-   [SwooleServer::addlistener](swoole-server.addlistener.html) — Додає нового слухача на сервер
-   [SwooleServer::addProcess](swoole-server.addprocess.html) — Додає певний користувачем swooleprocess на сервер
-   [SwooleServer::after](swoole-server.after.html) - Запускає callback-функцію після закінчення певного періоду часу
-   [SwooleServer::bind](swoole-server.bind.html) — Прив'язує з'єднання до вказаного ідентифікатора користувача
-   [SwooleServer::clearTimer](swoole-server.cleartimer.html) - Зупиняє та знищує таймер
-   [SwooleServer::close](swoole-server.close.html) - Закриває з'єднання з клієнтом
-   [SwooleServer::confirm](swoole-server.confirm.html) - Перевіряє стан з'єднання
-   [SwooleServer::connectioninfo](swoole-server.connection-info.html) — Отримує інформацію про з'єднання з описом файлу
-   [SwooleServer::connectionlist](swoole-server.connection-list.html) — Отримує всі встановлені з'єднання
-   [SwooleServer::construct](swoole-server.construct.html) - Створює сервер Swoole
-   [SwooleServer::defer](swoole-server.defer.html) — Відкладає виконання callback-функції наприкінці поточного EventLoop
-   [SwooleServerPort::construct](swoole-server-port.construct.html) - Створює порт сервера
-   [SwooleServerPort::destruct](swoole-server-port.destruct.html) — Знищує порт сервера
-   [SwooleServerPort::on](swoole-server-port.on.html) - Реєструє callback-функції події
-   [SwooleServerPort::set](swoole-server-port.set.html) — Встановлює протокол порту сервера
-   [SwooleServer::exist](swoole-server.exist.html) — Перевіряє, чи є з'єднання
-   [SwooleServer::finish](swoole-server.finish.html) — Використовується в процесі завдання для надсилання результату до робочого процесу після завершення завдання
-   [SwooleServer::getClientInfo](swoole-server.getclientinfo.html) — Отримує інформацію про з'єднання з описом файлу
-   [SwooleServer::getClientList](swoole-server.getclientlist.html) — Отримує всі встановлені з'єднання
-   [SwooleServer::getLastError](swoole-server.getlasterror.html) — Отримує код останньої помилки
-   [SwooleServer::heartbeat](swoole-server.heartbeat.html) — Перевіряє всі з'єднання на сервері
-   [SwooleServer::listen](swoole-server.listen.html) — Слухає по заданому IP та порту, тип сокету
-   [SwooleServer::on](swoole-server.on.html) - Реєструє callback-функцію на ім'я події
-   [SwooleServer::pause](swoole-server.pause.html) — Припиняє отримання даних від з'єднання
-   [SwooleServer::protect](swoole-server.protect.html) — Встановлює з'єднання у захищений режим
-   [SwooleServer::reload](swoole-server.reload.html) - Перезапускає всі робочі процеси
-   [SwooleServer::resume](swoole-server.resume.html) — Починає отримувати дані із з'єднання
-   [SwooleServer::send](swoole-server.send.html) — Надсилає дані клієнту
-   [SwooleServer::sendfile](swoole-server.sendfile.html) — Надсилає файл на з'єднання
-   [SwooleServer::sendMessage](swoole-server.sendmessage.html) — Надсилає повідомлення робочим процесам за ідентифікатором
-   [SwooleServer::sendto](swoole-server.sendto.html) — Надсилає дані на віддалену UDP-адресу
-   [SwooleServer::sendwait](swoole-server.sendwait.html) — Надсилає дані у віддалений сокет блокуючим способом
-   [SwooleServer::set](swoole-server.set.html) — Встановлює налаштування часу виконання сервера swoole
-   [SwooleServer::shutdown](swoole-server.shutdown.html) — Завершує процес головного сервера, функцію можна викликати у робочих процесах
-   [SwooleServer::start](swoole-server.start.html) - Запускає сервер Swoole
-   [SwooleServer::stats](swoole-server.stats.html) — Отримує статистику сервера Swoole
-   [SwooleServer::stop](swoole-server.stop.html) - Зупиняє сервер Swoole
-   [SwooleServer::task](swoole-server.task.html) — Надсилає дані до робочих процесів завдання
-   [SwooleServer::taskwait](swoole-server.taskwait.html) — Надсилає дані робочим процесам завдання блокуючим способом
-   [SwooleServer::taskWaitMulti](swoole-server.taskwaitmulti.html) — Виконує кілька завдань одночасно
-   [SwooleServer::tick](swoole-server.tick.html) — Повторює цю функцію у кожний заданий інтервал часу