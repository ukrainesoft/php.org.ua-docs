---
navigation:
  - gearmanclient.setoptions.md: '« GearmanClient::setOptions'
  - gearmanclient.settimeout.md: 'GearmanClient::setTimeout »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::setStatusCallback'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanClient::setStatusCallback

(PECL gearman >= 0.5.0)

GearmanClient::setStatusCallback - Завдання callback-функції, що збирає інформацію про стан обробника завдань

### Опис

```methodsynopsis
public GearmanClient::setStatusCallback(callable $function): bool
```

Задає callback-функцію, яка прийматиме і оброблятиме інформацію про стан завдання, що передається обробником завдань. Функція має приймати один аргумент типу [GearmanTask](class.gearmantask.md)

### Список параметрів

`function`

Функція виклику

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [GearmanClient::setDataCallback()](gearmanclient.setdatacallback.md) \- Задає callback-функцію обробки переданих даних
-   [GearmanClient::setCompleteCallback()](gearmanclient.setcompletecallback.md) \- Встановіть функцію, яка буде викликана після завершення завдання
-   [GearmanClient::setCreatedCallback()](gearmanclient.setcreatedcallback.md) \- Встановити функцію зворотного виклику, коли завдання ставиться у чергу
-   [GearmanClient::setExceptionCallback()](gearmanclient.setexceptioncallback.md) \- Встановлення функції зворотного дзвінка для перехоплення виключень обробника завдань
-   [GearmanClient::setFailCallback()](gearmanclient.setfailcallback.md) \- Установка callback-функції для обробки ситуації, коли завдання не вдалося виконати
-   [GearmanClient::setWarningCallback()](gearmanclient.setwarningcallback.md) \- Установка callback-функції, яка обслуговує попередження оброблювача завдань
-   [GearmanClient::setWorkloadCallback()](gearmanclient.setworkloadcallback.md) \- Установка callback-функції, яка приймає проміжні результати від оброблювача завдань
