---
navigation:
  - eventhttp.removeserveralias.md: '« EventHttp::removeServerAlias'
  - eventhttp.setcallback.md: 'EventHttp::setCallback »'
  - index.md: PHP Manual
  - class.eventhttp.md: EventHttp
title: 'EventHttp::setAllowedMethods'
---
# EventHttp::setAllowedMethods

(PECL event >= 1.4.0-beta)

EventHttp::setAllowedMethods — Встановлює, які методи HTTP підтримуються в запитах, прийнятих цим сервером і переданих callback-функції користувача

### Опис

```methodsynopsis
public
   EventHttp::setAllowedMethods(
    int
     $methods
   ): void
```

Встановлює, які методи HTTP підтримуються у запитах, прийнятих цим сервером та переданих callback-функції користувача.

Якщо не підтримується, видасть відповідь `"405 Method not allowed"`

За замовчуванням дозволено такі методи: `GET` `POST` `HEAD` `PUT` `DELETE` . Дивіться константи `EventHttpRequest::CMD_*`

### Список параметрів

`methods`

Бітова маска констант [`EventHttpRequest::CMD_*`](class.eventhttprequest.md#eventhttprequest.constants)

### Значення, що повертаються

Функція не повертає значення після виконання.
