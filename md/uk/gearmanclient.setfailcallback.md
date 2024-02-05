---
navigation:
  - gearmanclient.setexceptioncallback.md: '« GearmanClient::setExceptionCallback'
  - gearmanclient.setoptions.md: 'GearmanClient::setOptions »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::setFailCallback'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanClient::setFailCallback

(PECL gearman >= 0.5.0)

GearmanClient::setFailCallback — Встановлення callback-функції для обробки ситуації, коли завдання не вдалося виконати

### Опис

```methodsynopsis
public GearmanClient::setFailCallback(callable $function): bool
```

Задає функцію зворотного дзвінка для обробки ситуації, коли завдання виконати не вдалося. Приймає один аргумент типу [GearmanTask](class.gearmantask.md)

### Список параметрів

`function`

Функція виклику.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [GearmanClient::setDataCallback()](gearmanclient.setdatacallback.md) \- Задає callback-функцію обробки переданих даних
-   [GearmanClient::setCompleteCallback()](gearmanclient.setcompletecallback.md) \- Встановіть функцію, яка буде викликана після завершення завдання
-   [GearmanClient::setCreatedCallback()](gearmanclient.setcreatedcallback.md) \- Встановити функцію зворотного виклику, коли завдання ставиться у чергу
-   [GearmanClient::setExceptionCallback()](gearmanclient.setexceptioncallback.md) \- Встановлення функції зворотного дзвінка для перехоплення виключень обробника завдань
-   [GearmanClient::setStatusCallback()](gearmanclient.setstatuscallback.md) \- завдання callback-функції, що збирає інформацію про стан обробника завдань
-   [GearmanClient::setWarningCallback()](gearmanclient.setwarningcallback.md) \- Установка callback-функції, яка обслуговує попередження оброблювача завдань
-   [GearmanClient::setWorkloadCallback()](gearmanclient.setworkloadcallback.md) \- Установка callback-функції, яка приймає проміжні результати від оброблювача завдань
