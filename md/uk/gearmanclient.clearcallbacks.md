Очистити всі функції зворотного виклику цієї задачі

-   [« GearmanClient::addTaskStatus](gearmanclient.addtaskstatus.md)
    
-   [GearmanClient::clone »](gearmanclient.clone.md)
    
-   [PHP Manual](index.md)
    
-   [GearmanClient](class.gearmanclient.md)
    
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

-   [GearmanClient::setDataCallback()](gearmanclient.setdatacallback.md) - Задає callback-функцію обробки переданих даних
-   [GearmanClient::setCompleteCallback()](gearmanclient.setcompletecallback.md) - Встановіть функцію, яка буде викликана після завершення завдання
-   [GearmanClient::setCreatedCallback()](gearmanclient.setcreatedcallback.md) - Встановити функцію зворотного дзвінка, коли завдання ставиться в чергу
-   [GearmanClient::setExceptionCallback()](gearmanclient.setexceptioncallback.md) - Встановлення функції зворотного дзвінка для перехоплення виключень обробника завдань
-   [GearmanClient::setFailCallback()](gearmanclient.setfailcallback.md) - Установка callback-функції для обробки ситуації, коли завдання не вдалося виконати
-   [GearmanClient::setStatusCallback()](gearmanclient.setstatuscallback.md) - завдання callback-функції, що збирає інформацію про стан обробника завдань
-   [GearmanClient::setWarningCallback()](gearmanclient.setwarningcallback.md) - Установка callback-функції, яка обслуговує попередження оброблювача завдань
-   [GearmanClient::setWorkloadCallback()](gearmanclient.setworkloadcallback.md) - Установка callback-функції, яка приймає проміжні результати від оброблювача завдань