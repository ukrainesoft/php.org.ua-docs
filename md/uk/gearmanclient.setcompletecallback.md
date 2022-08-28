Встановіть функцію, яка буде викликана після завершення завдання

-   [« GearmanClient::setClientCallback](gearmanclient.setclientcallback.html)
    
-   [GearmanClient::setContext »](gearmanclient.setcontext.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanClient](class.gearmanclient.html)
    
-   Встановіть функцію, яка буде викликана після завершення завдання
    

# GearmanClient::setCompleteCallback

(PECL gearman >= 0.5.0)

GearmanClient::setCompleteCallback — Встановіть функцію, яка буде викликана після завершення завдання

### Опис

```methodsynopsis
public GearmanClient::setCompleteCallback(callable $callback): bool
```

Використовується для встановлення функції, яка буде викликана, коли [GearmanTask](class.gearmantask.html) буде виконано, або коли обробник викличе [GearmanJob::sendComplete()](gearmanjob.sendcomplete.html), Залежно від того, що трапиться раніше.

Ця callback-функція запускається тільки коли [GearmanTask](class.gearmantask.html) запущений з використанням [GearmanClient::runTasks()](gearmanclient.runtasks.html). Не використовується для індивідуальної роботи.

### Список параметрів

`callback`

Функція, яка має бути викликана.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanClient::setDataCallback()](gearmanclient.setdatacallback.html) - Задає callback-функцію обробки переданих даних
-   [GearmanClient::setCreatedCallback()](gearmanclient.setcreatedcallback.html) - Встановити функцію зворотного виклику, коли завдання ставиться у чергу
-   [GearmanClient::setExceptionCallback()](gearmanclient.setexceptioncallback.html) - Встановлення функції зворотного дзвінка для перехоплення виключень обробника завдань
-   [GearmanClient::setFailCallback()](gearmanclient.setfailcallback.html) - Установка callback-функції для обробки ситуації, коли завдання не вдалося виконати
-   [GearmanClient::setStatusCallback()](gearmanclient.setstatuscallback.html) - завдання callback-функції, що збирає інформацію про стан обробника завдань
-   [GearmanClient::setWarningCallback()](gearmanclient.setwarningcallback.html) - Установка callback-функції, яка обслуговує попередження оброблювача завдань
-   [GearmanClient::setWorkloadCallback()](gearmanclient.setworkloadcallback.html) - Установка callback-функції, яка приймає проміжні результати від оброблювача завдань