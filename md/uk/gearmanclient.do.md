Виконує одне завдання та повертає результат Застарілий метод

-   [« GearmanClient::data](gearmanclient.data.md)
    
-   [GearmanClient::doBackground »](gearmanclient.dobackground.md)
    
-   [PHP Manual](index.md)
    
-   [GearmanClient](class.gearmanclient.md)
    
-   Виконує одне завдання та повертає результат Застарілий метод
    

# GearmanClient::do

(PECL gearman >= 0.5.0)

GearmanClient::do — Виконує одне завдання та повертає результат Застарілий метод

### Опис

```methodsynopsis
public GearmanClient::do(string $function_name, string $workload, string $unique = ?): string
```

Метод **GearmanClient::do()** застарілий, починаючи з pecl/gearman 1.0.0. Використовуйте [GearmanClient::doNormal()](gearmanclient.donormal.md)

### Список параметрів

`function_name`

Зареєстрована функція, що викликається робочим процесом

`workload`

Серіалізовані дані, що підлягають обробці

`unique`

Унікальний ID, який призначається певному завданню

### Значення, що повертаються

Результат виконання завдання у вигляді рядка.

### Приклади

**Приклад #1 Просте подання завдання з безпосереднім поверненням**

```php
<?php

# Код клиента

echo "Начало\n";

# Создание клиента
$gmclient= new GearmanClient();

# Указание сервера по умолчанию (localhost).
$gmclient->addServer();

echo "Отправка задания\n";

$result = $gmclient->doNormal("reverse", "Hello!");

echo "Успешно: $result\n";

?>
```

```php
<?php

echo "Начало\n";

# Создание экземпляра обработчика
$gmworker= new GearmanWorker();

# Указание сервера по умолчанию (localhost).
$gmworker->addServer();

# Регистрация функции "reverse" на сервере. Изменение функции обработчика на
# "reverse_fn_fast" для более быстрой обработки без вывода.
$gmworker->addFunction("reverse", "reverse_fn");

print "Ожидание задания...\n";
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
  return strrev($job->workload());
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Начало
Отправка задания
Успешно: !olleH
```

**Приклад #2 Передача завдання та отримання інкрементного стану**

Надсилається завдання та встановлюється цикл для отримання інформації про зміну статусу. У обробника вказана штучна затримка для моделювання тривалого виконання завдання та задана відправка стану та даних під час обробки. Кожен наступний виклик **GearmanClient::do()** виводить інформацію про статус виконання поточного завдання.

```php
<?php

# Код клиента

# Создание экземпляра клиента Gearman
$gmclient= new GearmanClient();

# Указание сервера по умолчанию (localhost).
$gmclient->addServer();

echo "Отправка задания\n";

# Отправка задания reverse
do
{
  $result = $gmclient->doNormal("reverse", "Hello!");
  # Проверка на различные возвращаемые форматы и ошибки

  switch($gmclient->returnCode())
  {
    case GEARMAN_WORK_DATA:
      echo "Данные: $result\n";
      break;
    case GEARMAN_WORK_STATUS:
      list($numerator, $denominator)= $gmclient->doStatus();
      echo "Статус: $numerator/$denominator выполнено\n";
      break;
    case GEARMAN_WORK_FAIL:
      echo "Ошибка\n";
      exit;
    case GEARMAN_SUCCESS:
      break;
    default:
      echo "RET: " . $gmclient->returnCode() . "\n";
      echo "Error: " . $gmclient->error() . "\n";
      echo "Errno: " . $gmclient->getErrno() . "\n";
      exit;
  }
}
while($gmclient->returnCode() != GEARMAN_SUCCESS);

echo "Успешно: $result\n";

?>
```

```php
<?php

# Код обработчика

echo "Начало\n";

# Создание экземпляра обработчика.
$gmworker= new GearmanWorker();

# Указание сервера по умолчанию  (localhost).
$gmworker->addServer();

# Регистрация функции "reverse" на сервере.
$gmworker->addFunction("reverse", "reverse_fn");

print "Ожидание задания...\n";
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
  echo "Полученное задание: " . $job->handle() . "\n";

  $workload = $job->workload();
  $workload_size = $job->workloadSize();

  echo "Рабочая нагрузка: $workload ($workload_size)\n";

  # Данный цикл не является необходимым, только иллюстрирует процесс
  for ($x= 0; $x < $workload_size; $x++)
  {
    echo "Отправка статуса: " + $x + 1 . "/$workload_size выполнено\n";
    $job->sendStatus($x+1, $workload_size);
    $job->sendData(substr($workload, $x, 1));
    sleep(1);
  }

  $result= strrev($workload);
  echo "Результат: $result\n";

  # Возврат результата, отправляемого клиенту
  return $result;
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

Висновок оброблювача:

```
Начало
Ожидание задания...
Полученное задание: H:foo.local:106
Рабочая нагрузка: Hello! (6)
1/6 выполнено
2/6 выполнено
3/6 выполнено
4/6 выполнено
5/6 выполнено
6/6 выполнено
Результат: !olleH
```

Висновок клієнта:

```
Начало
Отправка задания
Статус: 1/6 выполнено
Данные: H
Статус: 2/6 выполнено
Данные: e
Статус: 3/6 выполнено
Данные: l
Статус: 4/6 выполнено
Данные: l
Статус: 5/6 выполнено
Данные: o
Статус: 6/6 выполнено
Данные: !
Успешно: !olleH
```

### Дивіться також

-   [GearmanClient::doHigh()](gearmanclient.dohigh.md) - Запускає на виконання завдання із високим пріоритетом
-   [GearmanClient::doLow()](gearmanclient.dolow.md) - Запускає виконання завдання з низьким пріоритетом
-   [GearmanClient::doBackground()](gearmanclient.dobackground.md) - Запускає виконання завдання у фоновому режимі
-   [GearmanClient::doHighBackground()](gearmanclient.dohighbackground.md) - Запускає на виконання із високим пріоритетом завдання у фоновому режимі
-   [GearmanClient::doLowBackground()](gearmanclient.dolowbackground.md) - Запускає на виконання з низьким пріоритетом завдання у фоновому режимі