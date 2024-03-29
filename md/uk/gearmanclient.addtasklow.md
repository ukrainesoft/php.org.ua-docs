---
navigation:
  - gearmanclient.addtaskhighbackground.md: '« GearmanClient::addTaskHighBackground'
  - gearmanclient.addtasklowbackground.md: 'GearmanClient::addTaskLowBackground »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::addTaskLow'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanClient::addTaskLow

(PECL gearman >= 0.5.0)

GearmanClient::addTaskLow — Додати низькопріоритетне завдання для роботи в паралельному режимі

### Опис

```methodsynopsis
public GearmanClient::addTaskLow(    string $function_name,    string|int|float $workload,    mixed $context = null,    ?string $unique_key = null): GearmanTask|false
```

Додає низькопріоритетне завдання для паралельної роботи з іншими завданнями. Викличте цей метод для всіх завдань, які працюватимуть паралельно, а потім викличте [GearmanClient::runTasks()](gearmanclient.runtasks.md) для виконання робіт. Завдання з низьким пріоритетом будуть вибрані з черги після завдань із нормальним або високим пріоритетом.

### Список параметрів

`function_name`

Зареєстрована функція, що викликається робочим процесом

`workload`

Серіалізовані дані, що підлягають обробці

`context`

Контекст програми, що пов'язується із завданням

`unique_key`

Унікальний ID, який призначається певному завданню

### Значення, що повертаються

Об'єкт [GearmanTask](class.gearmantask.md)или\*\*`false`\*\*, якщо завдання не може бути додано.

### Приклади

**Приклад #1 Низькопріоритетне завдання разом із двома звичайними завданнями**

Низькопріоритетне завдання включено серед двох інших завдань. Єдиний обробник доступний, так що завдання запускаються одна за одною, низькопріоритетні завдання виконуються в останню чергу.

```php
<?php

# создание клиента
$gmc= new GearmanClient();

# добавление сервера задач по умолчанию
$gmc->addServer();

# установка функции обратного вызова по завершению задачи
$gmc->setCompleteCallback("reverse_complete");

# добавление задач, одна из которых с низким приоритетом
$task= $gmc->addTask("reverse", "Hello World!", null, "1");
$task= $gmc->addTaskLow("reverse", "!dlroW olleH", null, "2");
$task= $gmc->addTask("reverse", "Hello World!", null, "3");

if (! $gmc->runTasks())
{
    echo "Ошибка " . $gmc->error() . "\n";
    exit;
}
echo "Готово\n";

function reverse_complete($task)
{
    echo "Выполнено: " . $task->unique() . ", " . $task->data() . "\n";
}

?>
```

Висновок наведеного прикладу буде схожим на:

```
Выполнено: 3, !dlroW olleH
Выполнено: 1, !dlroW olleH
Выполнено: 2, Hello World!
Готово
```

### Дивіться також

-   [GearmanClient::addTask()](gearmanclient.addtask.md) \- Додати завдання, яке буде виконано у паралельному режимі
-   [GearmanClient::addTaskHigh()](gearmanclient.addtaskhigh.md) \- Додати високопріоритетне завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskBackground()](gearmanclient.addtaskbackground.md) \- Додати фонове завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskHighBackground()](gearmanclient.addtaskhighbackground.md) \- Додати високопріоритетне фонове завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskLowBackground()](gearmanclient.addtasklowbackground.md) \- Додати низькопріоритетне фонове завдання для роботи в паралельному режимі
-   [GearmanClient::runTasks()](gearmanclient.runtasks.md) \- Запустити список завдань у паралельному режимі
