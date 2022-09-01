---
navigation:
  - gearmanclient.addtask.md: '« GearmanClient::addTask'
  - gearmanclient.addtaskhigh.md: 'GearmanClient::addTaskHigh »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::addTaskBackground'
---
# GearmanClient::addTaskBackground

(PECL gearman >= 0.5.0)

GearmanClient::addTaskBackground — Додати фонове завдання для роботи в паралельному режимі

### Опис

```methodsynopsis
public GearmanClient::addTaskBackground(    string $function_name,    string $workload,    mixed &$context = ?,    string $unique = ?): GearmanTask
```

Додає фонове завдання для паралельної роботи з іншими завданнями. Викличте цей метод для всіх завдань, які працюватимуть паралельно, а потім викличте [GearmanClient::runTasks()](gearmanclient.runtasks.md) для виконання робіт.

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

**Приклад #1 Два завдання, одне у фоновому режимі, а інше ні**

Цей приклад ілюструє різницю між виконанням фонової задачі і звичайним завданням. Клієнт додає дві задачі для виконання тих самих функцій, але одна додана за допомогою **addTaskBackground()**. Callback-функція встановлена ​​так, щоб виконання завдання можна було простежити. Простий обробник зі штучною затримкою повідомляє статус виконання завдання, і клієнт розуміє це через виклик callback-функції. Два обробники запущені для цього прикладу. Зверніть увагу, що фонове завдання не відображається у клієнтському висновку.

```php
<?php

# Клиентский скрипт

# Создание нашего клиента
$gmc= new GearmanClient();

# Добавление сервера задач по умолчанию
$gmc->addServer();

# Установка нескольких callback-функций. Таким образом, мы сможем отслеживать выполнение
$gmc->setCompleteCallback("reverse_complete");
$gmc->setStatusCallback("reverse_status");

# Добавление задачи для функции reverse
$task= $gmc->addTask("reverse", "Hello World!", null, "1");

# Добавление другой задачи, но она предназначена для запуска в фоновом режиме
$task= $gmc->addTaskBackground("reverse", "!dlroW olleH", null, "2");

if (! $gmc->runTasks())
{
    echo "Ошибка " . $gmc->error() . "\n";
    exit;
}

echo "Выполнено\n";

function reverse_status($task)
{
    echo "Статус: " . $task->unique() . ", " . $task->jobHandle() . " - " . $task->taskNumerator() .
         "/" . $task->taskDenominator() . "\n";
}

function reverse_complete($task)
{
    echo "Завершено: " . $task->unique() . ", " . $task->data() . "\n";
}

?>
```

```php
<?php

# Скрипт обработчика

echo "Начало\n";

# Создаём наш объект обработчика
$gmworker= new GearmanWorker();

# Добавление сервера задач по умолчанию (localhost).
$gmworker->addServer();

# Регистрируем функцию reverse на сервере
$gmworker->addFunction("reverse", "reverse_fn");

print "Ожидание задачи...\n";
while($gmworker->work())
{
  if ($gmworker->returnCode() != GEARMAN_SUCCESS)
  {
    echo "код возврата: " . $gmworker->returnCode() . "\n";
    break;
  }
}

function reverse_fn($job)
{
  echo "Полученная задача: " . $job->handle() . "\n";

  $workload = $job->workload();
  $workload_size = $job->workloadSize();

  echo "Рабочая нагрузка: $workload ($workload_size)\n";

  # В этом цикле для отображения статуса нет необходимости. Просто для демонстрации, как это работает
  for ($x= 0; $x < $workload_size; $x++)
  {
    echo "Отправка статуса: " . ($x + 1) . "/$workload_size выполнено\n";
    $job->sendStatus($x+1, $workload_size);
    $job->sendData(substr($workload, $x, 1));
    sleep(1);
  }

  $result= strrev($workload);
  echo "Результат: $result\n";

  # Возвращаем то, что мы хотим вернуть клиенту
  return $result;
}

?>
```

Виведення робітника для двох запущених працівників:

```
Полученная задача: H:foo.local:65
Рабочая нагрузка: !dlroW olleH (12)
1/12 выполнено
Полученная задача: H:foo.local:66
Рабочая нагрузка: Hello World! (12)
Отправка статуса: 1/12 выполнено
Отправка статуса: 2/12 выполнено
Отправка статуса: 2/12 выполнено
Отправка статуса: 3/12 выполнено
Отправка статуса: 3/12 выполнено
Отправка статуса: 4/12 выполнено
Отправка статуса: 4/12 выполнено
Отправка статуса: 5/12 выполнено
Отправка статуса: 5/12 выполнено
Отправка статуса: 6/12 выполнено
Отправка статуса: 6/12 выполнено
Отправка статуса: 7/12 выполнено
Отправка статуса: 7/12 выполнено
Отправка статуса: 8/12 выполнено
Отправка статуса: 8/12 выполнено
Отправка статуса: 9/12 выполнено
Отправка статуса: 9/12 выполнено
Отправка статуса: 10/12 выполнено
Отправка статуса: 10/12 выполнено
Отправка статуса: 11/12 выполнено
Отправка статуса: 11/12 выполнено
Отправка статуса: 12/12 выполнено
Отправка статуса: 12/12 выполнено
Результат: !dlroW olleH
Результат: Hello World!
```

Клієнт виводить:

```
Статус: 1, H:foo.local:66 - 1/12
Статус: 1, H:foo.local:66 - 2/12
Статус: 1, H:foo.local:66 - 3/12
Статус: 1, H:foo.local:66 - 4/12
Статус: 1, H:foo.local:66 - 5/12
Статус: 1, H:foo.local:66 - 6/12
Статус: 1, H:foo.local:66 - 7/12
Статус: 1, H:foo.local:66 - 8/12
Статус: 1, H:foo.local:66 - 9/12
Статус: 1, H:foo.local:66 - 10/12
Статус: 1, H:foo.local:66 - 11/12
Статус: 1, H:foo.local:66 - 12/12
Завершено: 1, !dlroW olleH
Выполнено
```

### Дивіться також

-   [GearmanClient::addTask()](gearmanclient.addtask.md) - Додати завдання, яке буде виконано у паралельному режимі
-   [GearmanClient::addTaskHigh()](gearmanclient.addtaskhigh.md) - Додати високопріоритетне завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskLow()](gearmanclient.addtasklow.md) - Додати низькопріоритетне завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskHighBackground()](gearmanclient.addtaskhighbackground.md) - Додати високопріоритетне фонове завдання для роботи в паралельному режимі
-   [GearmanClient::addTaskLowBackground()](gearmanclient.addtasklowbackground.md) - Додати низькопріоритетне фонове завдання для роботи в паралельному режимі
-   [GearmanClient::runTasks()](gearmanclient.runtasks.md) - Запустити список завдань у паралельному режимі
