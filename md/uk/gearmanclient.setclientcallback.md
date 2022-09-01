---
navigation:
  - gearmanclient.runtasks.md: '« GearmanClient::runTasks'
  - gearmanclient.setcompletecallback.md: 'GearmanClient::setCompleteCallback »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::setClientCallback'
---
# GearmanClient::setClientCallback

(PECL gearman <= 0.5.0)

GearmanClient::setClientCallback — Встановити функцію зворотного дзвінка, коли є пакет даних для завдання (застарілий метод)

### Опис

```methodsynopsis
public GearmanClient::setClientCallback(callable $callback): void
```

Встановлює функцію зворотного дзвінка для отримання пакетів даних для завдання. Функція зворотного виклику повинна приймати єдиний параметр – об'єкт [GearmanTask](class.gearmantask.md)

> **Зауваження**
> 
> Цей метод було замінено на [GearmanClient::setDataCallback()](gearmanclient.setdatacallback.md) у версії 0.6.0 модуля Gearman.

### Список параметрів

`callback`

Функція чи метод, які мають бути викликані.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanClient::setCompleteCallback()](gearmanclient.setcompletecallback.md) - Встановіть функцію, яка буде викликана після завершення завдання
-   [GearmanClient::setCreatedCallback()](gearmanclient.setcreatedcallback.md) - Встановити функцію зворотного виклику, коли завдання ставиться у чергу
-   [GearmanClient::setDataCallback()](gearmanclient.setdatacallback.md) - Задає callback-функцію обробки переданих даних
-   [GearmanClient::setExceptionCallback()](gearmanclient.setexceptioncallback.md) - Встановлення функції зворотного дзвінка для перехоплення виключень обробника завдань
-   [GearmanClient::setFailCallback()](gearmanclient.setfailcallback.md) - Установка callback-функції для обробки ситуації, коли завдання не вдалося виконати
-   [GearmanClient::setStatusCallback()](gearmanclient.setstatuscallback.md) - завдання callback-функції, що збирає інформацію про стан обробника завдань
-   [GearmanClient::setWarningCallback()](gearmanclient.setwarningcallback.md) - Установка callback-функції, яка обслуговує попередження оброблювача завдань
-   [GearmanClient::setWorkloadCallback()](gearmanclient.setworkloadcallback.md) - Установка callback-функції, яка приймає проміжні результати від оброблювача завдань
