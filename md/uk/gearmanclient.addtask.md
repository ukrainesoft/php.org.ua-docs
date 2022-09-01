---
navigation:
  - gearmanclient.addservers.md: '« GearmanClient::addServers'
  - gearmanclient.addtaskbackground.md: 'GearmanClient::addTaskBackground »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::addTask'
---
# GearmanClient::addTask

(PECL gearman >= 0.5.0)

GearmanClient::addTask — Додати завдання, яке буде виконане в паралельному режимі

### Опис

```methodsynopsis
public GearmanClient::addTask(    string $function_name,    string $workload,    mixed &$context = ?,    string $unique = ?): GearmanTask
```

Додає завдання для паралельної роботи з іншими завданнями. Викличте цей метод для всіх завдань, які працюватимуть паралельно, а потім викличте [GearmanClient::runTasks()](gearmanclient.runtasks.md) для виконання робіт. Зверніть увагу, що має бути достатня кількість обробників для одночасного виконання всіх завдань.

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

**Приклад #1 Основне уявлення двох завдань**

```php
<?php

# Создаём нашего клиента
$gmclient= new GearmanClient();

# Добавляем сервер задач по умолчанию
$gmclient->addServer();

# Устанавливаем функцию, которая будет вызвана по завершению работы
$gmclient->setCompleteCallback("complete");

# Добавляем задачу для выполнения функции reverse, переворачивающей строку "Hello World!"
$gmclient->addTask("reverse", "Hello World!", null, "1");

# Добавляем другую задачу, для выполнения функции reverse, переворачивающей строку "!dlroW olleH"
$gmclient->addTask("reverse", "!dlroW olleH", null, "2");

# Выполняем задачи
$gmclient->runTasks();

function complete($task)
{
  print "Выполнено: " . $task->unique() . ", " . $task->data() . "\n";
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Выполнено: 2, Hello World!
Выполнено: 1, !dlroW olleH
```

**Приклад #2 Основне уявлення двох завдань із передачею контексту програми**

```php
<?php

$client = new GearmanClient();
$client->addServer();

# Устанавливаем функцию, которая будет вызвана по завершению работы
$client->setCompleteCallback("reverse_complete");

# Добавим несколько задач и местоположение результатов
$results = array();
$client->addTask("reverse", "Hello World!", $results, "t1");
$client->addTask("reverse", "!dlroW olleH", $results, "t2");

$client->runTasks();

# Результаты должны быть заполнены из callback-функций
foreach ($results as $id => $result)
   echo $id . ": " . $result['handle'] . ", " . $result['data'] . "\n";


function reverse_complete($task, $results)
{
   $results[$task->unique()] = array("handle"=>$task->jobHandle(), "data"=>$task->data());
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
t2: H.foo:21, Hello World!
t1: H:foo:22, !dlroW olleH
```

### Дивіться також

-   [GearmanClient::addTaskHigh()](gearmanclient.addtaskhigh.md) - Додати високопріоритетне завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskLow()](gearmanclient.addtasklow.md) - Додати низькопріоритетне завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskBackground()](gearmanclient.addtaskbackground.md) - Додати фонове завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskHighBackground()](gearmanclient.addtaskhighbackground.md) - Додати високопріоритетне фонове завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskLowBackground()](gearmanclient.addtasklowbackground.md) - Додати низькопріоритетне фонове завдання для роботи в паралельному режимі
-   [GearmanClient::runTasks()](gearmanclient.runtasks.md) - Запустити список завдань у паралельному режимі
