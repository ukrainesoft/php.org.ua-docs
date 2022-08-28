Додати високопріоритетне фонове завдання для роботи в паралельному режимі

-   [« GearmanClient::addTaskHigh](gearmanclient.addtaskhigh.html)
    
-   [GearmanClient::addTaskLow »](gearmanclient.addtasklow.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanClient](class.gearmanclient.html)
    
-   Додати високопріоритетне фонове завдання для роботи в паралельному режимі
    

# GearmanClient::addTaskHighBackground

(PECL gearman >= 0.5.0)

GearmanClient::addTaskHighBackground — Додати високопріоритетне фонове завдання для роботи в паралельному режимі

### Опис

```methodsynopsis
public GearmanClient::addTaskHighBackground(    string $function_name,    string $workload,    mixed &$context = ?,    string $unique = ?): GearmanTask
```

Додає високопріоритетне фонове завдання для паралельної роботи з іншими завданнями. Викличте цей метод для всіх завдань, які працюватимуть паралельно, а потім викличте [GearmanClient::runTasks()](gearmanclient.runtasks.html) для виконання робіт. Завдання з високим пріоритетом будуть вибрані із черги раніше завдань із нормальним або низьким пріоритетом.

### Список параметрів

`function_name`

Зареєстрована функція, що викликається робочим процесом

`workload`

Серіалізовані дані, що підлягають обробці

`context`

Контекст програми, що пов'язується із завданням

`unique`

Унікальний ID, який призначається певному завданню

### Значення, що повертаються

Об'єкт [GearmanTask](class.gearmantask.html) або **`false`**, якщо завдання не може бути додано.

### Дивіться також

-   [GearmanClient::addTask()](gearmanclient.addtask.html) - Додати завдання, яке буде виконано у паралельному режимі
-   [GearmanClient::addTaskHigh()](gearmanclient.addtaskhigh.html) - Додати високопріоритетне завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskLow()](gearmanclient.addtasklow.html) - Додати низькопріоритетне завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskBackground()](gearmanclient.addtaskbackground.html) - Додати фонове завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskLowBackground()](gearmanclient.addtasklowbackground.html) - Додати низькопріоритетне фонове завдання для роботи в паралельному режимі
-   [GearmanClient::runTasks()](gearmanclient.runtasks.html) - Запустити список завдань у паралельному режимі