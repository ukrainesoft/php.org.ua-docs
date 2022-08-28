Установка callback-функції, що обслуговує попередження оброблювача завдань

-   [« GearmanClient::setTimeout](gearmanclient.settimeout.html)
    
-   [GearmanClient::setWorkloadCallback »](gearmanclient.setworkloadcallback.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanClient](class.gearmanclient.html)
    
-   Установка callback-функції, що обслуговує попередження оброблювача завдань
    

# GearmanClient::setWarningCallback

(PECL gearman >= 0.5.0)

GearmanClient::setWarningCallback — Встановлення callback-функції, яка обслуговує попередження оброблювача завдань

### Опис

```methodsynopsis
public GearmanClient::setWarningCallback(callable $callback): bool
```

Задає функцію, яка буде викликатись, коли обробник завдань надішле попередження. Функція має приймати один аргумент типу [GearmanTask](class.gearmantask.html)

### Список параметрів

`callback`

Функція зворотного дзвінка

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanClient::setDataCallback()](gearmanclient.setdatacallback.html) - Задає callback-функцію обробки переданих даних
-   [GearmanClient::setCompleteCallback()](gearmanclient.setcompletecallback.html) - Встановіть функцію, яка буде викликана після завершення завдання
-   [GearmanClient::setCreatedCallback()](gearmanclient.setcreatedcallback.html) - Встановити функцію зворотного виклику, коли завдання ставиться у чергу
-   [GearmanClient::setExceptionCallback()](gearmanclient.setexceptioncallback.html) - Встановлення функції зворотного дзвінка для перехоплення виключень обробника завдань
-   [GearmanClient::setFailCallback()](gearmanclient.setfailcallback.html) - Установка callback-функції для обробки ситуації, коли завдання не вдалося виконати
-   [GearmanClient::setStatusCallback()](gearmanclient.setstatuscallback.html) - завдання callback-функції, що збирає інформацію про стан обробника завдань
-   [GearmanClient::setWorkloadCallback()](gearmanclient.setworkloadcallback.html) - Установка callback-функції, яка приймає проміжні результати від оброблювача завдань