---
navigation:
  - gearman.examples.md: « Приклади
  - gearman.examples-reverse-bg.md: 'Базовий клієнт та обробник Gearman, фоновий режим »'
  - index.md: PHP Manual
  - gearman.examples.md: Приклади
title: Базове використання
---
## Базове використання

**Приклад #1 Базовий клієнт та обробник Gearman**

Цей приклад демонструє базову роботу з клієнтом та його обробником. Клієнт відправляє рядок серверу завдань, обробник перевертає рядок та відсилає його назад. Операція виконується синхронно.

```php
<?php

# Создание клиентского объекта
$gmclient= new GearmanClient();

# Указание сервера по умолчанию (localhost).
$gmclient->addServer();

echo "Sending job\n";

# Отправка задания обратно
do
{
  $result = $gmclient->doNormal("reverse", "Hello!");

  # Проверка на различные возвращаемые пакеты и ошибки.
  switch($gmclient->returnCode())
  {
    case GEARMAN_WORK_DATA:
      echo "Data: $result\n";
      break;
    case GEARMAN_WORK_STATUS:
      list($numerator, $denominator)= $gmclient->doStatus();
      echo "Status: $numerator/$denominator complete\n";
      break;
    case GEARMAN_WORK_FAIL:
      echo "Failed\n";
      exit;
    case GEARMAN_SUCCESS:
      echo "Success: $result\n";
      break;
    default:
      echo "RET: " . $gmclient->returnCode() . "\n";
      exit;
  }
}
while($gmclient->returnCode() != GEARMAN_SUCCESS);

?>
```

```php
<?php

echo "Starting\n";

# Создание нового обработчика.
$gmworker= new GearmanWorker();

# Добавление сервера по умолчанию (localhost).
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
Received job: H:foo.local:36
Workload: Hello! (6)
Sending status: 1/6 complete
Sending status: 2/6 complete
Sending status: 3/6 complete
Sending status: 4/6 complete
Sending status: 5/6 complete
Sending status: 6/6 complete
Result: !olleH
```

```
% php reverse_client.php
Starting
Sending job
Status: 1/6 complete
Status: 2/6 complete
Status: 3/6 complete
Status: 4/6 complete
Status: 5/6 complete
Status: 6/6 complete
Success: !olleH
```
