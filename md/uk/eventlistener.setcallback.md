- [« EventListener::getSocketName](eventlistener.getsocketname.md)
- [EventListener::setErrorCallback »](eventlistener.seterrorcallback.md)

- [PHP Manual](index.md)
- [EventListener](class.eventlistener.md)
- Ціль setCallback

# EventListener::setCallback

(PECL event \>= 1.2.6-beta)

EventListener::setCallback — Мета setCallback

### Опис

public **EventListener::setCallback**(
[callable](language.types.callable.md) `$cb` ,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$arg` = **`null`** ): void

Налаштуйте callback-функцію слухача події та, за необхідності,
callback-аргумент.

### Список параметрів

`cb`
Нова callback-функція для нових підключень. Ігнорується, якщо
**`null`**.

Повинна відповідати прототипу:

**callback**(
[EventListener](class.eventlistener.md) `$listener` = **`null`**
,

[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$fd` = **`null`** ,
array `$address` = **`null`** ,

[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$arg` = **`null`**
): void

`listener`
Об'єкт [EventListener](class.eventlistener.md).

`fd`
Файловий дескриптор чи ресурс, пов'язаний із слухачем.

`address`
Масив із двох елементів: IP-адреса та порт *server*.

`arg`
Ці дані, прикріплені до callback-функції.

`arg`
Ці дані, прикріплені до callback-функції. Ігнорується,
якщо **`null`**.

### Значення, що повертаються

Функція не повертає значення після виконання.
