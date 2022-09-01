---
navigation:
  - gearmanclient.addtasklow.md: '« GearmanClient::addTaskLow'
  - gearmanclient.addtaskstatus.md: 'GearmanClient::addTaskStatus »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::addTaskLowBackground'
---
# GearmanClient::addTaskLowBackground

(PECL gearman >= 0.5.0)

GearmanClient::addTaskLowBackground — Додати низькопріоритетне фонове завдання для роботи в паралельному режимі

### Опис

```methodsynopsis
public GearmanClient::addTaskLowBackground(    string $function_name,    string $workload,    mixed &$context = ?,    string $unique = ?): GearmanTask
```

Додає низькопріоритетне фонове завдання для паралельної роботи з іншими завданнями. Викличте цей метод для всіх завдань, які працюватимуть паралельно, а потім викличте [GearmanClient::runTasks()](gearmanclient.runtasks.md) для виконання робіт. Завдання з низьким пріоритетом будуть вибрані з черги після завдань із нормальним або високим пріоритетом.

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

### Дивіться також

-   [GearmanClient::addTask()](gearmanclient.addtask.md) - Додати завдання, яке буде виконано у паралельному режимі
-   [GearmanClient::addTaskHigh()](gearmanclient.addtaskhigh.md) - Додати високопріоритетне завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskLow()](gearmanclient.addtasklow.md) - Додати низькопріоритетне завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskBackground()](gearmanclient.addtaskbackground.md) - Додати фонове завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskHighBackground()](gearmanclient.addtaskhighbackground.md) - Додати високопріоритетне фонове завдання для роботи в паралельному режимі
-   [GearmanClient::runTasks()](gearmanclient.runtasks.md) - Запустити список завдань у паралельному режимі
