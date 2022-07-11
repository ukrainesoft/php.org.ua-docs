- [« swoole_error_log](function.swoole-error-log.md)
- [swoole_event_defer »](function.swoole-event-defer.md)

- [PHP Manual](index.md)
- [Функції Swoole](ref.swoole-funcs.md)
- Додати нових callback-функцій сокету до циклу подій

# swoole_event_add

(PECL swoole \>= 1.9.0)

swoole_event_add - Додати нових callback-функцій сокету в цикл подій

### Опис

**swoole_event_add**(
int `$fd`,
[callable](language.types.callable.md) `$read_callback` = ?,
[callable](language.types.callable.md) `$write_callback` = ?,
int `$events` = 0
): int

### Список параметрів

`fd`

`read_callback`

`write_callback`

`events`

### Значення, що повертаються
