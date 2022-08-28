Встановлення функції зворотного дзвінка для перехоплення виключень обробника завдань

-   [« GearmanClient::setDataCallback](gearmanclient.setdatacallback.html)
    
-   [GearmanClient::setFailCallback »](gearmanclient.setfailcallback.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanClient](class.gearmanclient.html)
    
-   Встановлення функції зворотного дзвінка для перехоплення виключень обробника завдань
    

# GearmanClient::setExceptionCallback

(PECL gearman >= 0.5.0)

GearmanClient::setExceptionCallback — Встановлення функції зворотного дзвінка для перехоплення виключень обробника завдань

### Опис

```methodsynopsis
public GearmanClient::setExceptionCallback(callable $callback): bool
```

Задає функцію, яка буде викликатись, коли обробник завдання відправить виняток.

### Список параметрів

`callback`

Функція перехоплення виключення, викинутого обробником завдань.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanClient::setDataCallback()](gearmanclient.setdatacallback.html) - Задає callback-функцію обробки переданих даних
-   [GearmanClient::setCompleteCallback()](gearmanclient.setcompletecallback.html) - Встановіть функцію, яка буде викликана після завершення завдання
-   [GearmanClient::setCreatedCallback()](gearmanclient.setcreatedcallback.html) - Встановити функцію зворотного виклику, коли завдання ставиться у чергу
-   [GearmanClient::setFailCallback()](gearmanclient.setfailcallback.html) - Установка callback-функції для обробки ситуації, коли завдання не вдалося виконати
-   [GearmanClient::setStatusCallback()](gearmanclient.setstatuscallback.html) - завдання callback-функції, що збирає інформацію про стан обробника завдань
-   [GearmanClient::setWarningCallback()](gearmanclient.setwarningcallback.html) - Установка callback-функції, яка обслуговує попередження оброблювача завдань
-   [GearmanClient::setWorkloadCallback()](gearmanclient.setworkloadcallback.html) - Установка callback-функції, яка приймає проміжні результати від оброблювача завдань