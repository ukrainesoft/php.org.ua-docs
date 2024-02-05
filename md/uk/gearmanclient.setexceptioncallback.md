---
navigation:
  - gearmanclient.setdatacallback.md: '« GearmanClient::setDataCallback'
  - gearmanclient.setfailcallback.md: 'GearmanClient::setFailCallback »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::setExceptionCallback'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanClient::setExceptionCallback

(PECL gearman >= 0.5.0)

GearmanClient::setExceptionCallback — Встановлення функції зворотного дзвінка для перехоплення виключень обробника завдань

### Опис

```methodsynopsis
public GearmanClient::setExceptionCallback(callable $function): bool
```

Задає функцію, яка буде викликатись, коли обробник завдання відправить виняток.

### Список параметрів

`function`

Функція перехоплення виключення, викинутого обробником завдань.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [GearmanClient::setDataCallback()](gearmanclient.setdatacallback.md) \- Задає callback-функцію обробки переданих даних
-   [GearmanClient::setCompleteCallback()](gearmanclient.setcompletecallback.md) \- Встановіть функцію, яка буде викликана після завершення завдання
-   [GearmanClient::setCreatedCallback()](gearmanclient.setcreatedcallback.md) \- Встановити функцію зворотного виклику, коли завдання ставиться у чергу
-   [GearmanClient::setFailCallback()](gearmanclient.setfailcallback.md) \- Установка callback-функції для обробки ситуації, коли завдання не вдалося виконати
-   [GearmanClient::setStatusCallback()](gearmanclient.setstatuscallback.md) \- завдання callback-функції, що збирає інформацію про стан обробника завдань
-   [GearmanClient::setWarningCallback()](gearmanclient.setwarningcallback.md) \- Установка callback-функції, яка обслуговує попередження оброблювача завдань
-   [GearmanClient::setWorkloadCallback()](gearmanclient.setworkloadcallback.md) \- Установка callback-функції, яка приймає проміжні результати від оброблювача завдань
