Базові клієнт та обробник Gearman, відправка завдань

-   [« Базовый клиент и обработчик Gearman, фоновый режим](gearman.examples-reverse-bg.html)
    
-   [GearmanClient »](class.gearmanclient.html)
    
-   [PHP Manual](index.html)
    
-   [Примеры](gearman.examples.html)
    
-   Базові клієнт та обробник Gearman, відправка завдань
    

## Базові клієнт та обробник Gearman, відправка завдань

**Приклад #1 Базові клієнт та обробник Gearman, відправлення завдань**

У цьому прикладі наш базовий клієнт перевертання рядка розширено так, щоб виконувати два завдання паралельно. Оброблювач перевертання рядка не змінений, за винятком додавання даних, що відправляються назад під час обробки.

```php
<?php

# создание клиента gearman
$gmc= new GearmanClient();

# указание сервера по умолчанию (localhost)
$gmc->addServer();

# регистрация функций обратного вызова
$gmc->setCreatedCallback("reverse_created");
$gmc->setDataCallback("reverse_data");
$gmc->setStatusCallback("reverse_status");
$gmc->setCompleteCallback("reverse_complete");
$gmc->setFailCallback("reverse_fail");

# указание неких произвольных данных
$data['foo'] = 'bar';

# добавление двух заданий
$task= $gmc->addTask("reverse", "foo", $data);
$task2= $gmc->addTaskLow("reverse", "bar", NULL);

# выполнение заданий параллельно (использование двух обработчиков)
if (! $gmc->runTasks())
{
    echo "ERROR " . $gmc->error() . "\n";
    exit;
}

echo "DONE\n";

function reverse_created($task)
{
    echo "CREATED: " . $task->jobHandle() . "\n";
}

function reverse_status($task)
{
    echo "STATUS: " . $task->jobHandle() . " - " . $task->taskNumerator() .
         "/" . $task->taskDenominator() . "\n";
}

function reverse_complete($task)
{
    echo "COMPLETE: " . $task->jobHandle() . ", " . $task->data() . "\n";
}

function reverse_fail($task)
{
    echo "FAILED: " . $task->jobHandle() . "\n";
}

function reverse_data($task)
{
    echo "DATA: " . $task->data() . "\n";
}

?>
```

```php
<?php

echo "Starting\n";

# Создание обработчика.
$gmworker= new GearmanWorker();

# Указание сервера по умолчанию  (localhost).
$gmworker->addServer();

# Регистрация функции "reverse" на сервере. Изменение функции обработчика на
# "reverse_fn_fast" для более быстрой обработки без вывода.
$gmworker->addFunction("reverse", "reverse_fn");

print "Waiting for job...\n";
while($gmworker->work())
{
  if ($gmworker->returnCode() != GEARMAN_SUCCESS)
  {
    echo "return_code: " . $gmworker->returnCode() . "\n";
    break;
  }
}

function reverse_fn($job)
{
  echo "Received job: " . $job->handle() . "\n";

  $workload = $job->workload();
  $workload_size = $job->workloadSize();

  echo "Workload: $workload ($workload_size)\n";

  # Этот цикл не является необходимым, но показывает как выполняется работа
  for ($x= 0; $x < $workload_size; $x++)
  {
    echo "Sending status: " . ($x + 1) . "/$workload_size complete\n";
    $job->sendStatus($x+1, $workload_size);
    $job->sendData(substr($workload, $x, 1));
    sleep(1);
  }

  $result= strrev($workload);
  echo "Result: $result\n";

  # Возвращаем, когда необходимо отправить результат обратно клиенту.
  return $result;
}

# Гораздо более простая и менее подробная версия вышеприведённой функции выглядит так:
function reverse_fn_fast($job)
{
  return strrev($job->workload());
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
% php reverse_worker.php
Starting
Waiting for job...
Received job: H:foo.local:45
Workload: foo (3)
1/3 complete
2/3 complete
3/3 complete
Result: oof
Received job: H:foo.local:44
Workload: bar (3)
1/3 complete
2/3 complete
3/3 complete
Result: rab
```

```
% php reverse_client_task.php
CREATED: H:foo.local:44
CREATED: H:foo.local:45
STATUS: H:foo.local:45 - 1/3
DATA: f
STATUS: H:foo.local:45 - 2/3
DATA: o
STATUS: H:foo.local:45 - 3/3
DATA: o
COMPLETE: H:foo.local:45, oof
STATUS: H:foo.local:44 - 1/3
DATA: b
STATUS: H:foo.local:44 - 2/3
DATA: a
STATUS: H:foo.local:44 - 3/3
DATA: r
COMPLETE: H:foo.local:44, rab
DONE
```