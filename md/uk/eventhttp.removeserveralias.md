---
navigation:
  - eventhttp.construct.md: '« EventHttp::\_\_construct'
  - eventhttp.setallowedmethods.md: 'EventHttp::setAllowedMethods »'
  - index.md: PHP Manual
  - class.eventhttp.md: EventHttp
title: 'EventHttp::removeServerAlias'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventHttp::removeServerAlias

(PECL event >= 1.4.0-beta)

EventHttp::removeServerAlias ​​— Видаляє псевдонім сервера

### Опис

```methodsynopsis
public
   EventHttp::removeServerAlias(
    string
     $alias
   ): bool
```

Видаляє псевдонім сервера, доданий за допомогою [EventHttp::addServerAlias()](eventhttp.addserveralias.md)

### Список параметрів

`alias`

Псевдонім для видалення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [EventHttp::addServerAlias()](eventhttp.addserveralias.md) \- Додає псевдонім сервера до об'єкта HTTP-сервера
