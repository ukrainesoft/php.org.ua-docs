Задає callback-функцію обробки переданих даних

-   [« GearmanClient::setData](gearmanclient.setdata.html)
    
-   [GearmanClient::setExceptionCallback »](gearmanclient.setexceptioncallback.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanClient](class.gearmanclient.html)
    
-   Задає callback-функцію обробки переданих даних
    

# GearmanClient::setDataCallback

(PECL gearman >= 0.6.0)

GearmanClient::setDataCallback — Задає функцію callback для обробки переданих даних

### Опис

```methodsynopsis
public GearmanClient::setDataCallback(callable $callback): bool
```

Задає callback-функцію, яка оброблятиме дані завдання. Ця функція повинна приймати один аргумент типу [GearmanTask](class.gearmantask.html)

### Список параметрів

`callback`

Функція або метод зворотного дзвінка.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanClient::setCompleteCallback()](gearmanclient.setcompletecallback.html) - Встановіть функцію, яка буде викликана після завершення завдання
-   [GearmanClient::setCreatedCallback()](gearmanclient.setcreatedcallback.html) - Встановити функцію зворотного дзвінка, коли завдання ставиться в чергу
-   [GearmanClient::setExceptionCallback()](gearmanclient.setexceptioncallback.html) - Встановлення функції зворотного дзвінка для перехоплення виключень обробника завдань
-   [GearmanClient::setFailCallback()](gearmanclient.setfailcallback.html) - Установка callback-функції для обробки ситуації, коли завдання не вдалося виконати
-   [GearmanClient::setStatusCallback()](gearmanclient.setstatuscallback.html) - завдання callback-функції, що збирає інформацію про стан обробника завдань
-   [GearmanClient::setWarningCallback()](gearmanclient.setwarningcallback.html) - Установка callback-функції, яка обслуговує попередження оброблювача завдань
-   [GearmanClient::setWorkloadCallback()](gearmanclient.setworkloadcallback.html) - Установка callback-функції, яка приймає проміжні результати від оброблювача завдань