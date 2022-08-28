Установка callback-функції для обробки ситуації, коли завдання не вдалося виконати

-   [« GearmanClient::setExceptionCallback](gearmanclient.setexceptioncallback.html)
    
-   [GearmanClient::setOptions »](gearmanclient.setoptions.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanClient](class.gearmanclient.html)
    
-   Установка callback-функції для обробки ситуації, коли завдання не вдалося виконати
    

# GearmanClient::setFailCallback

(PECL gearman >= 0.5.0)

GearmanClient::setFailCallback — Встановлення callback-функції для обробки ситуації, коли завдання не вдалося виконати

### Опис

```methodsynopsis
public GearmanClient::setFailCallback(callable $callback): bool
```

Задає функцію зворотного дзвінка для обробки ситуації, коли завдання виконати не вдалося. Приймає один аргумент типу [GearmanTask](class.gearmantask.html)

### Список параметрів

`callback`

Функція виклику.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanClient::setDataCallback()](gearmanclient.setdatacallback.html) - Задає callback-функцію обробки переданих даних
-   [GearmanClient::setCompleteCallback()](gearmanclient.setcompletecallback.html) - Встановіть функцію, яка буде викликана після завершення завдання
-   [GearmanClient::setCreatedCallback()](gearmanclient.setcreatedcallback.html) - Встановити функцію зворотного дзвінка, коли завдання ставиться в чергу
-   [GearmanClient::setExceptionCallback()](gearmanclient.setexceptioncallback.html) - Встановлення функції зворотного дзвінка для перехоплення виключень обробника завдань
-   [GearmanClient::setStatusCallback()](gearmanclient.setstatuscallback.html) - завдання callback-функції, що збирає інформацію про стан обробника завдань
-   [GearmanClient::setWarningCallback()](gearmanclient.setwarningcallback.html) - Установка callback-функції, яка обслуговує попередження оброблювача завдань
-   [GearmanClient::setWorkloadCallback()](gearmanclient.setworkloadcallback.html) - Установка callback-функції, яка приймає проміжні результати від оброблювача завдань