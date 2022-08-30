Друкує визначення класу PHP для інтерфейсу, що наслідує IDispatch

-   [« commessagepump](function.com-message-pump.html)
    
-   [variantabs »](function.variant-abs.html)
    
-   [PHP Manual](index.html)
    
-   [Функции COM](ref.com.html)
    
-   Друкує визначення класу PHP для інтерфейсу, що наслідує IDispatch
    

# comprinttypeinfo

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

comprinttypeinfo — Друкує визначення класу PHP для інтерфейсу, що наслідує IDispatch

### Опис

```methodsynopsis
com_print_typeinfo(variant|string $variant, ?string $dispatch_interface = null, bool $display_sink = false): bool
```

Призначення функції полягає у створенні "риби" класу для використання як приймача подій. Також ви можете використовувати її для створення заглушки для будь-якого об'єкта COM за умови, що він підтримує достатню кількість інтерфейсів самодіагностики, і що ви знаєте ім'я інтерфейсу, який ви хочете відобразити.

### Список параметрів

`variant`

`variant` повинен бути екземпляром класу COM, або ім'ям бібліотеки типів (яке буде розібрано згідно з набором правил, заданим у [comloadtypelib()](function.com-load-typelib.html)

`dispatch_interface`

Ім'я інтерфейсу, що наслідує `IDispatch`, який ви хочете відобразити.

`display_sink`

Якщо **`true`**, буде відображено відповідний інтерфейс приймача подій.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [comeventsink()](function.com-event-sink.html) - Зв'язати повідомлення COM з об'єктом PHP
-   [comloadtypelib()](function.com-load-typelib.html) - Завантаження Typelib