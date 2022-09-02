---
navigation:
  - gearmanworker.setoptions.md: '« GearmanWorker::setOptions'
  - gearmanworker.timeout.md: 'GearmanWorker::timeout »'
  - index.md: PHP Manual
  - class.gearmanworker.md: GearmanWorker
title: 'GearmanWorker::setTimeout'
---
# GearmanWorker::setTimeout

(PECL gearman >= 0.6.0)

GearmanWorker::setTimeout — Завдання часу очікування на введення/виведення на сокеті

### Опис

```methodsynopsis
public GearmanWorker::setTimeout(int $timeout): bool
```

Встановлює час очікування на активність на сокеті.

### Список параметрів

`timeout`

Тимчасовий інтервал у мілісекундах. Негативне значення вказує на відсутність обмежень.

### Значення, що повертаються

Завжди повертає **`true`**

### Приклади

**Приклад #1 Простий обробник із п'ятисекундним часом очікування**

```php
<?php

echo "Запуск\n";

# создаём объект обработчика.
$gmworker= new GearmanWorker();

# добавляем сервер по умолчанию (localhost).
$gmworker->addServer();

# регистрируем функцию "reverse" на сервере
$gmworker->addFunction("reverse", "reverse_fn");

# устанавливаем время ожидания 5 секунд
$gmworker->setTimeout(5000);

echo "Ожидание задания...\n";
while(@$gmworker->work() || $gmworker->returnCode() == GEARMAN_TIMEOUT)
{
  if ($gmworker->returnCode() == GEARMAN_TIMEOUT)
  {
    # Обычно хотелось бы сделать что-то полезное здесь ...
    echo "Время вышло. Ожидание следующего задания...\n";
    continue;
  }

  if ($gmworker->returnCode() != GEARMAN_SUCCESS)
  {
    echo "Код возврата: " . $gmworker->returnCode() . "\n";
    break;
  }
}

echo "Готово\n";

function reverse_fn($job)
{
  return strrev($job->workload());
}

?>
```

Якщо запустити цей обробник і не передавати йому завдань, висновок буде таким:

```
Запуск
Ожидание задания...
Время вышло. Ожидание следующего задания...
Время вышло. Ожидание следующего задания...
Время вышло. Ожидание следующего задания...
```

### Дивіться також

-   [GearmanWorker::timeout()](gearmanworker.timeout.md) - Отримання значення час очікування запитів на сокеті
