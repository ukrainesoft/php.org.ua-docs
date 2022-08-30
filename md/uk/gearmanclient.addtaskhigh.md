Додати високопріоритетне завдання для роботи в паралельному режимі

-   [« GearmanClient::addTaskBackground](gearmanclient.addtaskbackground.md)
    
-   [GearmanClient::addTaskHighBackground »](gearmanclient.addtaskhighbackground.md)
    
-   [PHP Manual](index.md)
    
-   [GearmanClient](class.gearmanclient.md)
    
-   Додати високопріоритетне завдання для роботи в паралельному режимі
    

# GearmanClient::addTaskHigh

(PECL gearman >= 0.5.0)

GearmanClient::addTaskHigh — Додати високопріоритетне завдання для роботи в паралельному режимі

### Опис

```methodsynopsis
public GearmanClient::addTaskHigh(    string $function_name,    string $workload,    mixed &$context = ?,    string $unique = ?): GearmanTask
```

Додає високопріоритетне завдання для паралельної роботи з іншими завданнями. Викличте цей метод для всіх високопріоритетних завдань, які працюватимуть паралельно, а потім викличте [GearmanClient::runTasks()](gearmanclient.runtasks.md) для виконання робіт. Завдання з високим пріоритетом будуть вибрані із черги раніше завдань із нормальним або низьким пріоритетом.

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

Об'єкт [GearmanTask](class.gearmantask.md) або **`false`**, якщо завдання не може бути додано.

### Приклади

**Приклад #1 Високопріоритетне завдання разом із двома звичайними завданнями**

Високопріоритетне завдання включено до двох інших завдань. Доступний єдиний обробник, тому завдання запускаються одна одною, високопріоритетні завдання виконуються насамперед.

```php
<?php

# создание клиента
$gmc= new GearmanClient();

# добавление сервера задач по умолчанию
$gmc->addServer();

# установка callback-функции для уведомления о завершении задачи
$gmc->setCompleteCallback("reverse_complete");

# добавление задач, одна из которых высокоприоритетная
$task= $gmc->addTask("reverse", "Hello World!", null, "1");
$task= $gmc->addTaskHigh("reverse", "!dlroW olleH", null, "2");
$task= $gmc->addTask("reverse", "Hello World!", null, "3");

if (! $gmc->runTasks())
{
    echo "Ошибка " . $gmc->error() . "\n";
    exit;
}
echo "Выполнено\n";

function reverse_complete($task)
{
    echo "Завершено: " . $task->unique() . ", " . $task->data() . "\n";
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Завершено: 2, Hello World!
Завершено: 3, !dlroW olleH
Завершено: 1, !dlroW olleH
Выполнено
```

### Дивіться також

-   [GearmanClient::addTask()](gearmanclient.addtask.md) - Додати завдання, яке буде виконано у паралельному режимі
-   [GearmanClient::addTaskLow()](gearmanclient.addtasklow.md) - Додати низькопріоритетне завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskBackground()](gearmanclient.addtaskbackground.md) - Додати фонове завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskHighBackground()](gearmanclient.addtaskhighbackground.md) - Додати високопріоритетне фонове завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskLowBackground()](gearmanclient.addtasklowbackground.md) - Додати низькопріоритетне фонове завдання для роботи в паралельному режимі
-   [GearmanClient::runTasks()](gearmanclient.runtasks.md) - Запустити список завдань у паралельному режимі