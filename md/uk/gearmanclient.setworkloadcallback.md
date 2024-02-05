---
navigation:
  - gearmanclient.setwarningcallback.md: '« GearmanClient::setWarningCallback'
  - gearmanclient.timeout.md: 'GearmanClient::timeout »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::setWorkloadCallback'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanClient::setWorkloadCallback

(PECL gearman >= 0.5.0)

GearmanClient::setWorkloadCallback — Встановлення callback-функції, яка приймає проміжні результати від обробника завдань

### Опис

```methodsynopsis
public GearmanClient::setWorkloadCallback(callable $function): bool
```

Задає функцію, яка буде викликатись, коли обробнику завдання необхідно передати проміжні результати клієнту до завершення всієї обробки. Обробнику завдань може знадобитися таке пересилання, якщо потрібно передати клієнту будь-які оновлення, частково надіслати результати обробки або звільнити пам'ять під час виконання довгих завдань. Функція має приймати один аргумент типу [GearmanTask](class.gearmantask.md)

### Список параметрів

`function`

Callback-функція.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [GearmanClient::setDataCallback()](gearmanclient.setdatacallback.md) \- Задає callback-функцію обробки переданих даних
-   [GearmanClient::setCompleteCallback()](gearmanclient.setcompletecallback.md) \- Встановіть функцію, яка буде викликана після завершення завдання
-   [GearmanClient::setCreatedCallback()](gearmanclient.setcreatedcallback.md) \- Встановити функцію зворотного виклику, коли завдання ставиться у чергу
-   [GearmanClient::setExceptionCallback()](gearmanclient.setexceptioncallback.md) \- Встановлення функції зворотного дзвінка для перехоплення виключень обробника завдань
-   [GearmanClient::setFailCallback()](gearmanclient.setfailcallback.md) \- Установка callback-функції для обробки ситуації, коли завдання не вдалося виконати
-   [GearmanClient::setStatusCallback()](gearmanclient.setstatuscallback.md) \- завдання callback-функції, що збирає інформацію про стан обробника завдань
-   [GearmanClient::setWarningCallback()](gearmanclient.setwarningcallback.md) \- Установка callback-функції, яка обслуговує попередження оброблювача завдань
