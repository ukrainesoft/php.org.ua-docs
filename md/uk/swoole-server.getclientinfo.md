- [« Swoole\Server::finish](swoole-server.finish.md)
- [Swoole\Server::getClientList »](swoole-server.getclientlist.md)

- [PHP Manual](index.md)
- [Swoole\Server](class.swoole-server.md)
- Отримує інформацію про з'єднання з описом файлу

# Swoole\Server::getClientInfo

(PECL swoole \>= 1.9.0)

Swoole\Server::getClientInfo — Отримує інформацію про з'єднання з
опис файлу

### Опис

public **Swoole\Server::getClientInfo**(int `$fd`, int `$reactor_id` =
?, bool `$ignore_error` = ?): array

### Список параметрів

`fd`
Дескриптор файлу

`reactor_id`
Ідентифікатор потоку Reactor, у якому виконується з'єднання.

`ignore_error`
Чи слід ігнорувати помилки. Якщо встановлено значення true,
інформація про з'єднання буде повернена, навіть якщо з'єднання буде
закрито.

### Значення, що повертаються
