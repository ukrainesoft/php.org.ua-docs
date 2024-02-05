---
navigation:
  - gearmanclient.setclientcallback.md: '« GearmanClient::setClientCallback'
  - gearmanclient.setcontext.md: 'GearmanClient::setContext »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::setCompleteCallback'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanClient::setCompleteCallback

(PECL gearman >= 0.5.0)

GearmanClient::setCompleteCallback — Встановіть функцію, яка буде викликана після завершення завдання

### Опис

```methodsynopsis
public GearmanClient::setCompleteCallback(callable $function): bool
```

Використовується для встановлення функції, яка буде викликана, коли [GearmanTask](class.gearmantask.md) буде виконано, або коли обробник викличе [GearmanJob::sendComplete()](gearmanjob.sendcomplete.md), Залежно від того, що трапиться раніше.

Ця callback-функція запускається тільки коли [GearmanTask](class.gearmantask.md)запущен с использованием[GearmanClient::runTasks()](gearmanclient.runtasks.md). Не використовується для індивідуальної роботи.

### Список параметрів

`function`

Функція, яка має бути викликана.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [GearmanClient::setDataCallback()](gearmanclient.setdatacallback.md) \- Задає callback-функцію обробки переданих даних
-   [GearmanClient::setCreatedCallback()](gearmanclient.setcreatedcallback.md) \- Встановити функцію зворотного виклику, коли завдання ставиться у чергу
-   [GearmanClient::setExceptionCallback()](gearmanclient.setexceptioncallback.md) \- Встановлення функції зворотного дзвінка для перехоплення виключень обробника завдань
-   [GearmanClient::setFailCallback()](gearmanclient.setfailcallback.md) \- Установка callback-функції для обробки ситуації, коли завдання не вдалося виконати
-   [GearmanClient::setStatusCallback()](gearmanclient.setstatuscallback.md) \- завдання callback-функції, що збирає інформацію про стан обробника завдань
-   [GearmanClient::setWarningCallback()](gearmanclient.setwarningcallback.md) \- Установка callback-функції, яка обслуговує попередження оброблювача завдань
-   [GearmanClient::setWorkloadCallback()](gearmanclient.setworkloadcallback.md) \- Установка callback-функції, яка приймає проміжні результати від оброблювача завдань
