- [« Swoole\Http\Response::write](swoole-http-response.write.md)
- [Swoole\Http\Server::on »](swoole-http-server.on.md)

- [PHP Manual](index.md)
- [Swoole](book.swoole.md)
- Клас Swoole \ Http \ Server

# Клас Swoole\Http\Server

(PECL swoole \>= 1.9.0)

## Вступ

## Огляд класів

class **Swoole\Http\Server** extends
[Swoole\Server](class.swoole-server.md) {

/\* Методи \*/

public [on](swoole-http-server.on.md)(string `$event_name`,
[callable](language.types.callable.md) `$callback`): void

public [start](swoole-http-server.start.md)(): void

/\* Наслідувані методи \*/

public
[Swoole\Server::addlistener](swoole-server.addlistener.md)(string
`$host`, int `$port`, string `$socket_type`): void

public
[Swoole\Server::addProcess](swoole-server.addprocess.md)([swoole_process](class.swoole-process.md)
`$process`): bool

public [Swoole\Server::after](swoole-server.after.md)(int
`$after_time_ms`, [callable](language.types.callable.md) `$callback`,
string `$param` = ?): ReturnType

public [Swoole\Server::bind](swoole-server.bind.md)(int `$fd`, int
`$uid`): bool

public [Swoole\Server::clearTimer](swoole-server.cleartimer.md)(int
`$timer_id`): void

**swoole_timer_clear**(int `$timer_id`): void

public [Swoole\Server::close](swoole-server.close.md)(int `$fd`, bool
`$reset` = ?): bool

public [Swoole\Server::confirm](swoole-server.confirm.md)(int `$fd`):
bool

public
[Swoole\Server::connection_info](swoole-server.connection-info.md)(int
`$fd`, int `$reactor_id` = ?): array

public
[Swoole\Server::connection_list](swoole-server.connection-list.md)(int
`$start_fd`, int `$pagesize` = ?): array

public
[Swoole\Server::defer](swoole-server.defer.md)([callable](language.types.callable.md)
`$callback`): void

public
[Swoole\Server\Port::\_\_destruct](swoole-server-port.destruct.md)():
void

public [Swoole\Server\Port::on](swoole-server-port.on.md)(string
`$event_name`, [callable](language.types.callable.md) `$callback`):
ReturnType

public [Swoole\Server\Port::set](swoole-server-port.set.md)(array
`$settings`): void

public [Swoole\Server::exist](swoole-server.exist.md)(int `$fd`): bool

public [Swoole\Server::finish](swoole-server.finish.md)(string
`$data`): void

public
[Swoole\Server::getClientInfo](swoole-server.getclientinfo.md)(int
`$fd`, int `$reactor_id` = ?, bool `$ignore_error` = ?): array

public
[Swoole\Server::getClientList](swoole-server.getclientlist.md)(int
`$start_fd`, int `$pagesize` = ?): array

public [Swoole\Server::getLastError](swoole-server.getlasterror.md)():
int

public [Swoole\Server::heartbeat](swoole-server.heartbeat.md)(bool
`$if_close_connection`):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

public [Swoole\Server::listen](swoole-server.listen.md)(string
`$host`, int `$port`, string `$socket_type`): bool

public [Swoole\Server::on](swoole-server.on.md)(string `$event_name`,
[callable](language.types.callable.md) `$callback`): void

public [Swoole\Server::pause](swoole-server.pause.md)(int `$fd`): void

public [Swoole\Server::protect](swoole-server.protect.md)(int `$fd`,
bool `$is_protected` = ?): void

public [Swoole\Server::reload](swoole-server.reload.md)(): bool

public [Swoole\Server::resume](swoole-server.resume.md)(int `$fd`):
void

public [Swoole\Server::send](swoole-server.send.md)(int `$fd`, string
`$data`, int `$reactor_id` = ?): bool

public [Swoole\Server::sendfile](swoole-server.sendfile.md)(int `$fd`,
string `$filename`, int `$offset` = ?): bool

public [Swoole\Server::sendMessage](swoole-server.sendmessage.md)(int
`$worker_id`, string `$data`): bool

public [Swoole\Server::sendto](swoole-server.sendto.md)(
string `$ip`,
int `$port`,
string `$data`,
string `$server_socket` = ?
): bool

public [Swoole\Server::sendwait](swoole-server.sendwait.md)(int `$fd`,
string `$data`): bool

public [Swoole\Server::set](swoole-server.set.md)(array `$settings`):
ReturnType

public [Swoole\Server::shutdown](swoole-server.shutdown.md)(): void

public [Swoole\Server::start](swoole-server.start.md)(): void

public [Swoole\Server::stats](swoole-server.stats.md)(): array

public [Swoole\Server::stop](swoole-server.stop.md)(int `$worker_id` =
?): bool

public [Swoole\Server::task](swoole-server.task.md)(string `$data`,
int `$dst_worker_id` = ?, [callable](language.types.callable.md)
`$callback` = ?):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

public [Swoole\Server::taskwait](swoole-server.taskwait.md)(string
`$data`, float `$timeout` = ?, int `$worker_id` = ?): void

public
[Swoole\Server::taskWaitMulti](swoole-server.taskwaitmulti.md)(array
`$tasks`, double `$timeout_ms` = ?): void

public [Swoole\Server::tick](swoole-server.tick.md)(int
`$interval_ms`, [callable](language.types.callable.md) `$callback`):
void

}

## Зміст

- [Swoole\Http\Server::on](swoole-http-server.on.md) - Прив'язує
callback-функцію до HTTP-серверу на ім'я події
- [Swoole\Http\Server::start](swoole-http-server.start.md) -
Запускає http-сервер swoole
