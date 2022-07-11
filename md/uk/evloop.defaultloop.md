- [«EvLoop::\_\_construct](evloop.construct.md)
- [EvLoop::embed »](evloop.embed.md)

- [PHP Manual](index.md)
- [EvLoop](class.evloop.md)
- Повертає або створює цикл за замовчуванням

# EvLoop::defaultLoop

(PECL ev \>= 0.2.0)

EvLoop::defaultLoop — Повертає або створює цикл стандартних подій

### Опис

public static **EvLoop::defaultLoop**(
int `$flags` = Ev::FLAG_AUTO ,

[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$data` = NULL ,
float `$io_interval` = 0. ,
float `$timeout_interval` = 0.
): [EvLoop](class.evloop.md)

Якщо цикл стандартних подій не створено, **EvLoop::defaultLoop()**
створює його із зазначеними параметрами. Інакше він просто
повертає об'єкт, який представляє раніше створений екземпляр, ігноруючи
всі параметри.

### Список параметрів

`flags`
Один з [прапорів циклу подій](class.ev.md#ev.constants.loop-flags)

`data`
Дані користувача, пов'язані з циклом.

`io_collect_interval`
Дивіться [io_interval](class.evloop.md#evloop.props.io-interval)

`timeout_collect_interval`
Дивіться
[timeout_interval](class.evloop.md#evloop.props.timeout-interval)

### Значення, що повертаються

Повертає об'єкт EvLoop у разі успішного виконання.

### Дивіться також

- [EvLoop::\_\_construct()](evloop.construct.md) - Конструктор
об'єкта циклу подій
