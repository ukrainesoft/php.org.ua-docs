---
navigation:
  - eventhttprequest.addheader.md: '« EventHttpRequest::addHeader'
  - eventhttprequest.clearheaders.md: 'EventHttpRequest::clearHeaders »'
  - index.md: PHP Manual
  - class.eventhttprequest.md: EventHttpRequest
title: 'EventHttpRequest::cancel'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventHttpRequest::cancel

(PECL event >= 1.4.0-beta)

EventHttpRequest::cancel — Скасує очікування HTTP-запиту

### Опис

```methodsynopsis
public
   EventHttpRequest::cancel(): void
```

Скасує очікування HTTP-запиту.

Скасує поточний запит HTTP. Callback-функція, пов'язана із цим запитом, не виконається, об'єкт запиту звільняється. Якщо запит на даний час обробляється, наприклад, безперервний запит, відповідний об'єкт [EventHttpConnection](class.eventhttpconnection.md)будет сброшен.

Запит не може бути скасовано, якщо його callback-функція вже виконана. Запит може бути анульований повторно з його фрагментованої callback-функції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.
