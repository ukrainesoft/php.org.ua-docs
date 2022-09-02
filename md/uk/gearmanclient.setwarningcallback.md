---
navigation:
  - gearmanclient.settimeout.md: '« GearmanClient::setTimeout'
  - gearmanclient.setworkloadcallback.md: 'GearmanClient::setWorkloadCallback »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::setWarningCallback'
---
# GearmanClient::setWarningCallback

(PECL gearman >= 0.5.0)

GearmanClient::setWarningCallback — Встановлення callback-функції, яка обслуговує попередження оброблювача завдань

### Опис

```methodsynopsis
public GearmanClient::setWarningCallback(callable $callback): bool
```

Задає функцію, яка буде викликатись, коли обробник завдань надішле попередження. Функція має приймати один аргумент типу [GearmanTask](class.gearmantask.md)

### Список параметрів

`callback`

Функція зворотного дзвінка

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanClient::setDataCallback()](gearmanclient.setdatacallback.md) - Задає callback-функцію обробки переданих даних
-   [GearmanClient::setCompleteCallback()](gearmanclient.setcompletecallback.md) - Встановіть функцію, яка буде викликана після завершення завдання
-   [GearmanClient::setCreatedCallback()](gearmanclient.setcreatedcallback.md) - Встановити функцію зворотного виклику, коли завдання ставиться у чергу
-   [GearmanClient::setExceptionCallback()](gearmanclient.setexceptioncallback.md) - Встановлення функції зворотного дзвінка для перехоплення виключень обробника завдань
-   [GearmanClient::setFailCallback()](gearmanclient.setfailcallback.md) - Установка callback-функції для обробки ситуації, коли завдання не вдалося виконати
-   [GearmanClient::setStatusCallback()](gearmanclient.setstatuscallback.md) - завдання callback-функції, що збирає інформацію про стан обробника завдань
-   [GearmanClient::setWorkloadCallback()](gearmanclient.setworkloadcallback.md) - Установка callback-функції, яка приймає проміжні результати від оброблювача завдань
