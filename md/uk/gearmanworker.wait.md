Очікування запиту з одного із сервера завдань

-   [« GearmanWorker::unregisterAll](gearmanworker.unregisterall.html)
    
-   [GearmanWorker::work »](gearmanworker.work.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanWorker](class.gearmanworker.html)
    
-   Очікування запиту з одного із сервера завдань
    

# GearmanWorker::wait

(PECL gearman >= 0.6.0)

GearmanWorker::wait — Очікування запиту з одного із сервера завдань

### Опис

```methodsynopsis
public GearmanWorker::wait(): bool
```

При роботі в неблокуючому режимі введення/виводу змушує оброблювача чекати завдання від сервера завдань Gearman. У разі відмови буде видано попередження **`E_WARNING`** із зазначенням останньої помилки, що відбулася.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Запуск оброблювача в режимі неблокування**

```php
<?php

echo "Запуск\n";

# создание объекта обработчика
$worker= new GearmanWorker();

# включение неблокирующего режима
$worker->addOptions(GEARMAN_WORKER_NON_BLOCKING);

# добавление сервера по умолчанию (localhost на порту 4730)
$worker->addServer();

# добавление callback-функции
$worker->addFunction('reverse', 'reverse_fn');

# попробуем получить задание
while (@$worker->work() ||
       $worker->returnCode() == GEARMAN_IO_WAIT ||
       $worker->returnCode() == GEARMAN_NO_JOBS)
{
  if ($worker->returnCode() == GEARMAN_SUCCESS)
    continue;

  echo "Ожидание следующего задания...\n";
  if (!@$worker->wait())
  {
    if ($worker->returnCode() == GEARMAN_NO_ACTIVE_FDS)
    {
      # мы не подключены ни к одному из серверов, подождём немного
      # и попробуем переподключиться
      sleep(5);
      continue;
    }
    break;
  }
}

echo "Ошибка в обработчике: " . $worker->error() . "\n";

function reverse_fn($job)
{
  return strrev($job->workload());
}


?>
```

### Дивіться також

-   [GearmanWorker::work()](gearmanworker.work.html) - Очікування та виконання завдань