---
navigation:
  - swoole-channel.stats.md: '« SwooleChannel::stats'
  - swoole-client.close.md: 'SwooleClient::close »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас SwooleClient
---
# Клас SwooleClient

(PECL swoole >= 1.9.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class Swoole\Client
     
     {

    /* Constants */
    
     const
     int
      MSG_OOB = 1;

    const
     int
      MSG_PEEK = 2;

    const
     int
      MSG_DONTWAIT = 128;

    const
     int
      MSG_WAITALL = 64;


    /* Свойства */
    public
      $errCode;

    public
      $sock;

    public
      $reuse;

    public
      $reuseCount;



    /* Методы */
    
   public close(bool $force = ?): bool
public connect(    string $host,    int $port = ?,    int $timeout = ?,    int $flag = ?): bool
public __destruct(): void
public getpeername(): array
public getsockname(): array
public isConnected(): bool
public on(string $event, callable $callback): void
public pause(): void
public pipe(string $socket): void
public recv(string $size = ?, string $flag = ?): void
public resume(): void
public send(string $data, string $flag = ?): int
public sendfile(string $filename, int $offset = ?): bool
public sendto(string $ip, int $port, string $data): bool
public set(array $settings): void
public sleep(): void
public wakeup(): void

   }
```

## Властивості

errCode

sock

reuse

reuseCount

## Обумовлені константи

**`Swoole\Client::MSG_OOB`**

**`Swoole\Client::MSG_PEEK`**

**`Swoole\Client::MSG_DONTWAIT`**

**`Swoole\Client::MSG_WAITALL`**

## Зміст

-   [SwooleClient::close](swoole-client.close.md) — Закриває встановлене з'єднання
-   [SwooleClient::connect](swoole-client.connect.md) — Підключається до віддаленого порту TCP або UDP
-   [SwooleClient::construct](swoole-client.construct.md) — Створює синхронний або асинхронний TCP/UDP клієнт Swoole із підтримкою SSL або без нього
-   [SwooleClient::destruct](swoole-client.destruct.md) - Знищує клієнт Swoole
-   [SwooleClient::getpeername](swoole-client.getpeername.md) — Отримує ім'я віддаленого сокету з'єднання
-   [SwooleClient::getsockname](swoole-client.getsockname.md) — Отримує локальне ім'я сокета з'єднання
-   [SwooleClient::isConnected](swoole-client.isconnected.md) — Перевіряє, чи з'єднання встановлено.
-   [SwooleClient::on](swoole-client.on.md) — Додає callback-функції, спричинені подіями
-   [SwooleClient::pause](swoole-client.pause.md) — Припиняє отримання даних
-   [SwooleClient::pipe](swoole-client.pipe.md) — Перенаправляє дані до іншого файлового дескриптора.
-   [SwooleClient::recv](swoole-client.recv.md) — Отримує дані із віддаленого сокету
-   [SwooleClient::resume](swoole-client.resume.md) — Відновлює отримання даних
-   [SwooleClient::send](swoole-client.send.md) — Надсилає дані у віддалений TCP-сокет
-   [SwooleClient::sendfile](swoole-client.sendfile.md) — Надсилає файл у віддалений TCP-сокет
-   [SwooleClient::sendto](swoole-client.sendto.md) — Надсилає дані на віддалену UDP-адресу
-   [SwooleClient::set](swoole-client.set.md) — Встановлює параметри Swoole до встановлення з'єднання
-   [SwooleClient::sleep](swoole-client.sleep.md) — Видаляє TCP-клієнт із циклу системних подій
-   [SwooleClient::wakeup](swoole-client.wakeup.md) — Додає TCP-клієнт назад у цикл системних подій
