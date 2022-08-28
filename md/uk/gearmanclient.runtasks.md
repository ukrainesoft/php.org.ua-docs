Запустити список завдань у паралельному режимі

-   [« GearmanClient::returnCode](gearmanclient.returncode.html)
    
-   [GearmanClient::setClientCallback »](gearmanclient.setclientcallback.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanClient](class.gearmanclient.html)
    
-   Запустити список завдань у паралельному режимі
    

# GearmanClient::runTasks

(PECL gearman >= 0.5.0)

GearmanClient::runTasks — Запустити список завдань у паралельному режимі

### Опис

```methodsynopsis
public GearmanClient::runTasks(): bool
```

Для набору завдань, раніше доданих за допомогою [GearmanClient::addTask()](gearmanclient.addtask.html) [GearmanClient::addTaskHigh()](gearmanclient.addtaskhigh.html) [GearmanClient::addTaskLow()](gearmanclient.addtasklow.html) [GearmanClient::addTaskBackground()](gearmanclient.addtaskbackground.html) [GearmanClient::addTaskHighBackground()](gearmanclient.addtaskhighbackground.html) або [GearmanClient::addTaskLowBackground()](gearmanclient.addtasklowbackground.html), цей виклик починається в паралельному режимі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanClient::addTask()](gearmanclient.addtask.html) - Додати завдання, яке буде виконано у паралельному режимі