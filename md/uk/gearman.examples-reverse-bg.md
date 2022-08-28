Базовий клієнт та обробник Gearman, фоновий режим

-   [« Базовое использование](gearman.examples-reverse.html)
    
-   [Базовые клиент и обработчик Gearman, отправка задач »](gearman.examples-reverse-task.html)
    
-   [PHP Manual](index.html)
    
-   [Примеры](gearman.examples.html)
    
-   Базовий клієнт та обробник Gearman, фоновий режим
    

## Базовий клієнт та обробник Gearman, фоновий режим

**Приклад #1 Базовий клієнт та обробник Gearman, фоновий режим**

Цей приклад демонструє базову роботу з клієнтом та його обробником. Клієнт відправляє рядок серверу виконання завдань у вигляді фонового завдання, а обробник перевертає рядок. Зверніть увагу, робота виконується асинхронно, тобто. клієнт не чекає завершення завдання, а одразу відключається (а значить і не отримує результату).

```php
<?php

# создание объекта
$gmclient= new GearmanClient();

# указание сервера по умолчанию (localhost)
$gmclient->addServer();

# выполнение в фоновом режиме
$job_handle = $gmclient->doBackground("reverse", "this is a test");

if ($gmclient->returnCode() != GEARMAN_SUCCESS)
{
  echo "bad return code\n";
  exit;
}

echo "done!\n";

?>
```

```php
<?php

echo "Starting\n";

# Создание обработчика.
$gmworker= new GearmanWorker();

# Указание сервера по умолчанию (localhost).
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
    $job->sendStatus($x, $workload_size);
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
Received job: H:foo.local:41
Workload: this is a test (14)
1/14 complete
2/14 complete
3/14 complete
4/14 complete
5/14 complete
6/14 complete
7/14 complete
8/14 complete
9/14 complete
10/14 complete
11/14 complete
12/14 complete
13/14 complete
14/14 complete
Result: tset a si siht
```

```
% php reverse_client_bg.php
done!
```