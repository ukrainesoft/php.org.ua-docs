Очистити всі функції зворотного виклику цієї задачі

-   [« GearmanClient::addTaskStatus](gearmanclient.addtaskstatus.html)
    
-   [GearmanClient::clone »](gearmanclient.clone.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanClient](class.gearmanclient.html)
    
-   Очистити всі функції зворотного виклику цієї задачі
    

# GearmanClient::clearCallbacks

(PECL gearman >= 0.5.0)

GearmanClient::clearCallbacks — Очистити всі функції зворотного виклику цієї задачі

### Опис

```methodsynopsis
public GearmanClient::clearCallbacks(): bool
```

Очищає всі callback-функції завдання, які були встановлені раніше.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Завжди повертає **`true`**

### Дивіться також

-   [GearmanClient::setDataCallback()](gearmanclient.setdatacallback.html) - Задає callback-функцію обробки переданих даних
-   [GearmanClient::setCompleteCallback()](gearmanclient.setcompletecallback.html) - Встановіть функцію, яка буде викликана після завершення завдання
-   [GearmanClient::setCreatedCallback()](gearmanclient.setcreatedcallback.html) - Встановити функцію зворотного дзвінка, коли завдання ставиться в чергу
-   [GearmanClient::setExceptionCallback()](gearmanclient.setexceptioncallback.html) - Встановлення функції зворотного дзвінка для перехоплення виключень обробника завдань
-   [GearmanClient::setFailCallback()](gearmanclient.setfailcallback.html) - Установка callback-функції для обробки ситуації, коли завдання не вдалося виконати
-   [GearmanClient::setStatusCallback()](gearmanclient.setstatuscallback.html) - завдання callback-функції, що збирає інформацію про стан обробника завдань
-   [GearmanClient::setWarningCallback()](gearmanclient.setwarningcallback.html) - Установка callback-функції, яка обслуговує попередження оброблювача завдань
-   [GearmanClient::setWorkloadCallback()](gearmanclient.setworkloadcallback.html) - Установка callback-функції, яка приймає проміжні результати від оброблювача завдань