---
navigation:
  - eventbufferevent.getenabled.md: '« EventBufferEvent::getEnabled'
  - eventbufferevent.getoutput.md: 'EventBufferEvent::getOutput »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::getInput'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBufferEvent::getInput

(PECL event >= 1.2.6-beta)

EventBufferEvent::getInput — Повертає базовий вхідний буфер, пов'язаний із поточною буферною подією

### Опис

```methodsynopsis
public
   EventBufferEvent::getInput(): EventBuffer
```

Повертає базовий вхідний буфер, пов'язаний із поточною буферною подією. Вхідний буфер - це сховище для читання.

Зверніть увагу, що є також `[input](class.eventbufferevent.md#eventbufferevent.props.input)`свойство класса[EventBufferEvent](class.eventbufferevent.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає екземпляр класу [EventBuffer](class.eventbuffer.md) вхідного буфера, пов'язаного із поточною буферною подією.

### Приклади

**Приклад #1 Callback-функція читання буфера**

```php
<?php
function readcb($bev, $base) {
    $input = $bev->input; //$bev->getInput();

    while (($n = $input->remove($buf, 1024)) > 0) {
        echo $buf;
    }
}
?>
```

### Дивіться також

-   [EventBufferEvent::getOutput()](eventbufferevent.getoutput.md) \- Повертає базовий вихідний буфер, пов'язаний із поточною буферною подією
