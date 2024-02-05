---
navigation:
  - gearmanclient.setcontext.md: '« GearmanClient::setContext'
  - gearmanclient.setdata.md: 'GearmanClient::setData »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::setCreatedCallback'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanClient::setCreatedCallback

(PECL gearman >= 0.5.0)

GearmanClient::setCreatedCallback — Встановити функцію зворотного виклику, коли завдання ставиться в чергу

### Опис

```methodsynopsis
public GearmanClient::setCreatedCallback(callable $function): bool
```

Встановлює функцію, яка буде викликана, коли завдання отримано та поставлено в чергу сервером задач Gearman. Функція зворотного виклику повинна приймати єдиний параметр – об'єкт [GearmanTask](class.gearmantask.md)

### Список параметрів

`function`

Функція, яка має бути викликана.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [GearmanClient::setDataCallback()](gearmanclient.setdatacallback.md) \- Задає callback-функцію обробки переданих даних
-   [GearmanClient::setCompleteCallback()](gearmanclient.setcompletecallback.md) \- Встановіть функцію, яка буде викликана після завершення завдання
-   [GearmanClient::setExceptionCallback()](gearmanclient.setexceptioncallback.md) \- Встановлення функції зворотного дзвінка для перехоплення виключень обробника завдань
-   [GearmanClient::setFailCallback()](gearmanclient.setfailcallback.md) \- Установка callback-функції для обробки ситуації, коли завдання не вдалося виконати
-   [GearmanClient::setStatusCallback()](gearmanclient.setstatuscallback.md) \- завдання callback-функції, що збирає інформацію про стан обробника завдань
-   [GearmanClient::setWarningCallback()](gearmanclient.setwarningcallback.md) \- Установка callback-функції, яка обслуговує попередження оброблювача завдань
-   [GearmanClient::setWorkloadCallback()](gearmanclient.setworkloadcallback.md) \- Установка callback-функції, яка приймає проміжні результати від оброблювача завдань
