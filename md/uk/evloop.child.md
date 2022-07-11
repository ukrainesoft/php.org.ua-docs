- [«EvLoop::check](evloop.check.md)
- [EvLoop::\_\_construct »](evloop.construct.md)

- [PHP Manual](index.md)
- [EvLoop](class.evloop.md)
- Створює об'єкт EvChild, пов'язаний із поточним циклом подій

# EvLoop::child

(PECL ev \>= 0.2.0)

EvLoop::child — Створює об'єкт EvChild, пов'язаний із поточним циклом
подій

### Опис

final public **EvLoop::child**(
string `$pid` ,
string `$trace` ,
string `$callback`,
string `$data` = ?,
string `$priority` = ?
): [EvChild](class.evchild.md)

Створює об'єкт EvChild, пов'язаний із поточним циклом подій.

### Список параметрів

Усі параметри, що й для
[EvChild::\_\_construct()](evchild.construct.md)

### Значення, що повертаються

Повертає об'єкт EvChild у разі успішного виконання.

### Дивіться також

- [EvChild::\_\_construct()](evchild.construct.md) - Створює об'єкт
спостерігач EvChild
