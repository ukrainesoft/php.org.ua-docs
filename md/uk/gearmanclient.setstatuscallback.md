---
navigation:
  - gearmanclient.setoptions.html: '« GearmanClient::setOptions'
  - gearmanclient.settimeout.html: 'GearmanClient::setTimeout »'
  - index.html: PHP Manual
  - class.gearmanclient.html: GearmanClient
title: 'GearmanClient::setStatusCallback'
---
# GearmanClient::setStatusCallback

(PECL gearman >= 0.5.0)

GearmanClient::setStatusCallback - Завдання callback-функції, що збирає інформацію про стан обробника завдань

### Опис

```methodsynopsis
public GearmanClient::setStatusCallback(callable $callback): bool
```

Задає callback-функцію, яка прийматиме і оброблятиме інформацію про стан завдання, що передається обробником завдань. Функція має приймати один аргумент типу [GearmanTask](class.gearmantask.html)

### Список параметрів

`callback`

Функція виклику

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanClient::setDataCallback()](gearmanclient.setdatacallback.html) - Задає callback-функцію обробки переданих даних
-   [GearmanClient::setCompleteCallback()](gearmanclient.setcompletecallback.html) - Встановіть функцію, яка буде викликана після завершення завдання
-   [GearmanClient::setCreatedCallback()](gearmanclient.setcreatedcallback.html) - Встановити функцію зворотного дзвінка, коли завдання ставиться в чергу
-   [GearmanClient::setExceptionCallback()](gearmanclient.setexceptioncallback.html) - Встановлення функції зворотного дзвінка для перехоплення виключень обробника завдань
-   [GearmanClient::setFailCallback()](gearmanclient.setfailcallback.html) - Установка callback-функції для обробки ситуації, коли завдання не вдалося виконати
-   [GearmanClient::setWarningCallback()](gearmanclient.setwarningcallback.html) - Установка callback-функції, яка обслуговує попередження оброблювача завдань
-   [GearmanClient::setWorkloadCallback()](gearmanclient.setworkloadcallback.html) - Установка callback-функції, яка приймає проміжні результати від оброблювача завдань
