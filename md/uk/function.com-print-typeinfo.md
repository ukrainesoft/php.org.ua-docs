---
navigation:
  - function.com-message-pump.md: « com\_message\_pump
  - function.variant-abs.md: variant\_abs »
  - index.md: PHP Manual
  - ref.com.md: Функції COM
title: com\_print\_typeinfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# com\_print\_typeinfo

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

com\_print\_typeinfo — Друкує визначення класу PHP для інтерфейсу, що наслідує IDispatch

### Опис

```methodsynopsis
com_print_typeinfo(variant|string $variant, ?string $dispatch_interface = null, bool $display_sink = false): bool
```

Призначення функції полягає у створенні "риби" класу для використання як приймача подій. Також ви можете використовувати її для створення заглушки для будь-якого об'єкта COM за умови, що він підтримує достатню кількість інтерфейсів самодіагностики, і що ви знаєте ім'я інтерфейсу, який ви хочете відобразити.

### Список параметрів

`variant`

`variant` повинен бути екземпляром класу COM, або ім'ям бібліотеки типів (яке буде розібрано згідно з набором правил, заданим у [com\_load\_typelib()](function.com-load-typelib.md)

`dispatch_interface`

Ім'я інтерфейсу, що наслідує `IDispatch`, який ви хочете відобразити.

`display_sink`

Якщо **`true`**, буде відображено відповідний інтерфейс приймача подій.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [com\_event\_sink()](function.com-event-sink.md) \- Зв'язати повідомлення COM з об'єктом PHP
-   [com\_load\_typelib()](function.com-load-typelib.md) \- Завантаження Typelib
