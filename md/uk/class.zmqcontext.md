- [«ZMQ::\_\_construct](zmq.construct.md)
- [ZMQContext::\_\_construct »](zmqcontext.construct.md)

- [PHP Manual](index.md)
- [Обмін повідомленнями 0MQ](book.zmq.md)
- Клас ZMQContext

# Клас ZMQContext

(PECL zmq \>= 0.5.0)

## Вступ

## Огляд класів

class **ZMQContext** {

/\* Методи \*/

public [\_\_construct](zmqcontext.construct.md)(int `$io_threads` = 1,
bool `$is_persistent` = **`true`**)

public [getOpt](zmqcontext.getopt.md)(string `$key`):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

public [getSocket](zmqcontext.getsocket.md)(int `$type`, string
`$persistent_id` = **`null`**, [callable](language.types.callable.md)
`$on_new_socket` = **`null`**): [ZMQSocket](class.zmqsocket.md)

public [isPersistent](zmqcontext.ispersistent.md)(): bool

public [setOpt](zmqcontext.setopt.md)(int `$key`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$value`): [ZMQContext](class.zmqcontext.md)

}

## Зміст

- [ZMQContext::\_\_construct](zmqcontext.construct.md) - Конструктор
ZMQContext
- [ZMQContext::getOpt](zmqcontext.getopt.md) — Отримати опцію
контексту
- [ZMQContext::getSocket](zmqcontext.getsocket.md) — Створює новий
сокет
- [ZMQContext::isPersistent](zmqcontext.ispersistent.md) — Є
чи контекст постійним
- [ZMQContext::setOpt](zmqcontext.setopt.md) — Встановити опцію
сокету
