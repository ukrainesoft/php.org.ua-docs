---
navigation:
  - swoole-http-response.write.md: '« Swoole\\Http\\Response::write'
  - swoole-http-server.on.md: 'Swoole\\Http\\Server::on »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас Swoole\\Http\\Server
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Swoole\\Http\\Server

(PECL swoole >= 1.9.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class Swoole\Http\Server
     

     
      extends
       Swoole\Server
     
     {


    /* Методы */
    
            public on(string $event_name, callable $callback): void
public start(): void


    /* Наследуемые методы */
    public Swoole\Server::addlistener(string $host, int $port, string $socket_type): void
public Swoole\Server::addProcess(swoole_process $process): bool
public Swoole\Server::after(int $after_time_ms, callable $callback, string $param = ?): ReturnType
public Swoole\Server::bind(int $fd, int $uid): bool
public Swoole\Server::clearTimer(int $timer_id): void
swoole_timer_clear(int $timer_id): void
public Swoole\Server::close(int $fd, bool $reset = ?): bool
public Swoole\Server::confirm(int $fd): bool
public Swoole\Server::connection_info(int $fd, int $reactor_id = ?): array
public Swoole\Server::connection_list(int $start_fd, int $pagesize = ?): array
public Swoole\Server::defer(callable $callback): void
public Swoole\Server\Port::__destruct(): void
public Swoole\Server\Port::on(string $event_name, callable $callback): ReturnType
public Swoole\Server\Port::set(array $settings): void
public Swoole\Server::exist(int $fd): bool
public Swoole\Server::finish(string $data): void
public Swoole\Server::getClientInfo(int $fd, int $reactor_id = ?, bool $ignore_error = ?): array
public Swoole\Server::getClientList(int $start_fd, int $pagesize = ?): array
public Swoole\Server::getLastError(): int
public Swoole\Server::heartbeat(bool $if_close_connection): mixed
public Swoole\Server::listen(string $host, int $port, string $socket_type): bool
public Swoole\Server::on(string $event_name, callable $callback): void
public Swoole\Server::pause(int $fd): void
public Swoole\Server::protect(int $fd, bool $is_protected = ?): void
public Swoole\Server::reload(): bool
public Swoole\Server::resume(int $fd): void
public Swoole\Server::send(int $fd, string $data, int $reactor_id = ?): bool
public Swoole\Server::sendfile(int $fd, string $filename, int $offset = ?): bool
public Swoole\Server::sendMessage(int $worker_id, string $data): bool
public Swoole\Server::sendto(    string $ip,    int $port,    string $data,    string $server_socket = ?): bool
public Swoole\Server::sendwait(int $fd, string $data): bool
public Swoole\Server::set(array $settings): ReturnType
public Swoole\Server::shutdown(): void
public Swoole\Server::start(): void
public Swoole\Server::stats(): array
public Swoole\Server::stop(int $worker_id = ?): bool
public Swoole\Server::task(string $data, int $dst_worker_id = ?, callable $callback = ?): mixed
public Swoole\Server::taskwait(string $data, float $timeout = ?, int $worker_id = ?): void
public Swoole\Server::taskWaitMulti(array $tasks, float $timeout_ms = ?): void
public Swoole\Server::tick(int $interval_ms, callable $callback): void


   }
```

## Зміст

-   [Swoole\\Http\\Server::on](swoole-http-server.on.md)— Прив'язує callback-функцію до HTTP-сервера на ім'я події
-   [Swoole\\Http\\Server::start](swoole-http-server.start.md) \- Запускає http-сервер swoole
