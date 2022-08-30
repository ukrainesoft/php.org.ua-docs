Виконує одиночне завдання та повертає результат

-   [« GearmanClient::doLowBackground](gearmanclient.dolowbackground.md)
    
-   [GearmanClient::doStatus »](gearmanclient.dostatus.md)
    
-   [PHP Manual](index.md)
    
-   [GearmanClient](class.gearmanclient.md)
    
-   Виконує одиночне завдання та повертає результат
    

# GearmanClient::doNormal

(No version information available, might only be in Git)

GearmanClient::doNormal — Виконує одиночне завдання та повертає результат

### Опис

```methodsynopsis
public GearmanClient::doNormal(string $function_name, string $workload, string $unique = ?): string
```

Виконує одиночне завдання та повертає рядкове подання результату. Формат результату, що повертається, визначають об'єкти. [GearmanClient](class.gearmanclient.md) і [GearmanWorker](class.gearmanworker.md)

### Список параметрів

`function_name`

Зареєстрована функція, що викликається робочим процесом

`workload`

Серіалізовані дані, що підлягають обробці

`unique`

Унікальний ID, який призначається певному завданню

### Значення, що повертаються

Рядок, що представляє результат виконання завдання.

### Приклади

**Приклад #1 Виконання простого завдання з негайним поверненням**

```php
<?php

?>
```

```php
<?php

# Код клиента

echo "Запуск\n";

# Создание клиента.
$gmclient= new GearmanClient();

# Добавление сервера по умолчанию (localhost).
$gmclient->addServer();

echo "Отправка задания\n";

$result = $gmclient->doNormal("reverse", "Hello!");

echo "Задание выполнено: $result\n";

?>
```

```php
<?php

echo "Запуск\n";

# Создание объекта обработчика заданий.
$gmworker= new GearmanWorker();

# Добавление сервера по умолчанию (localhost).
$gmworker->addServer();

# Регистрация функции "reverse" на сервере. Замена обрабатывающей функции
# на "reverse_fn_fast" для быстрой обработки без вывода
$gmworker->addFunction("reverse", "reverse_fn");

print "Ожидание задания...\n";
while($gmworker->work())
{
  if ($gmworker->returnCode() != GEARMAN_SUCCESS)
  {
    echo "Код возврата: " . $gmworker->returnCode() . "\n";
    break;
  }
}

function reverse_fn($job)
{
  return strrev($job->workload());
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Запуск
Отправка задания
Задание выполнено: !olleH
```

**Приклад #2 Надсилання завдання на обробку та моніторинг стану**

Після надсилання завдання скрипт у циклі запитує поточний прогрес обробки. В обробник введена штучна затримка, щоб змоделювати завдання, що довго виконується. Оброблювач посилає клієнту свій поточний стан, як тільки завершено обробку чергової порції даних. Послідовні виклики **GearmanClient::doNormal()** запитують поточний стан завдання, що виконується.

```php
<?php

# Код клиента

# Создание клиента.
$gmclient= new GearmanClient();

# Добавление сервера по умолчанию (localhost).
$gmclient->addServer();

echo "Отправка задания\n";

# Отправка задания перевернуть строку
do
{
  $result = $gmclient->doNormal("reverse", "Hello!");
  # Проверка состояния на ошибки или возвращаемые данные.

  switch($gmclient->returnCode())
  {
    case GEARMAN_WORK_DATA:
      echo "Данные: $result\n";
      break;
    case GEARMAN_WORK_STATUS:
      list($numerator, $denominator)= $gmclient->doStatus();
      echo "Статус: $numerator/$denominator complete\n";
      break;
    case GEARMAN_WORK_FAIL:
      echo "Ошибка\n";
      exit;
    case GEARMAN_SUCCESS:
      break;
    default:
      echo "Код возврата: " . $gmclient->returnCode() . "\n";
      echo "Ошибка: " . $gmclient->error() . "\n";
      echo "Номер ошибки: " . $gmclient->getErrno() . "\n";
      exit;
  }
}
while($gmclient->returnCode() != GEARMAN_SUCCESS);

echo "Обработка завершена: $result\n";

?>
```

```php
<?php

# Код обработчика

echo "Запуск\n";

# Создаём свой объект обработчика.
$gmworker= new GearmanWorker();

# Добавление сервера по умолчанию (localhost).
$gmworker->addServer();

# Регистрируем функцию "reverse" на сервере.
$gmworker->addFunction("reverse", "reverse_fn");

print "Ожидание задания...\n";
while($gmworker->work())
{
  if ($gmworker->returnCode() != GEARMAN_SUCCESS)
  {
    echo "Код возврата: " . $gmworker->returnCode() . "\n";
    break;
  }
}

function reverse_fn($job)
{
  echo "Получено задание: " . $job->handle() . "\n";

  $workload = $job->workload();
  $workload_size = $job->workloadSize();

  echo "Загружены данные: $workload ($workload_size)\n";

  # Этот цикл не является необходимым, просто показывает, как все работает
  for ($x= 0; $x < $workload_size; $x++)
  {
    echo "Отправка статуса: " + $x + 1 . "/$workload_size завершено\n";
    $job->sendStatus($x+1, $workload_size);
    $job->sendData(substr($workload, $x, 1));
    sleep(1);
  }

  $result= strrev($workload);
  echo "Результат: $result\n";

  # Возвращаем то, что хотим отправить клиенту
  return $result;
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

Висновок оброблювача:

```
Запуск
Ожидание задания...
Получено задание: H:foo.local:106
Загружены данные: Hello! (6)
1/6 завершено
2/6 завершено
3/6 завершено
4/6 завершено
5/6 завершено
6/6 завершено
Результат: !olleH
```

Висновок клієнта:

```
Запуск
Отправка задания
Состояние: 1/6 завершено
Данные: H
Состояние: 2/6 завершено
Данные: e
Состояние: 3/6 завершено
Данные: l
Состояние: 4/6 завершено
Данные: l
Состояние: 5/6 завершено
Данные: o
Состояние: 6/6 завершено
Данные: !
Обработка завершена: !olleH
```

### Дивіться також

-   [GearmanClient::doHigh()](gearmanclient.dohigh.md) - Запускає на виконання завдання із високим пріоритетом
-   [GearmanClient::doLow()](gearmanclient.dolow.md) - Запускає виконання завдання з низьким пріоритетом
-   [GearmanClient::doBackground()](gearmanclient.dobackground.md) - Запускає виконання завдання у фоновому режимі
-   [GearmanClient::doHighBackground()](gearmanclient.dohighbackground.md) - Запускає на виконання із високим пріоритетом завдання у фоновому режимі
-   [GearmanClient::doLowBackground()](gearmanclient.dolowbackground.md) - Запускає на виконання з низьким пріоритетом завдання у фоновому режимі