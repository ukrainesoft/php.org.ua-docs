---
navigation:
  - gearmanclient.donormal.md: '« GearmanClient::doNormal'
  - gearmanclient.echo.md: 'GearmanClient::echo »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::doStatus'
---
# GearmanClient::doStatus

(PECL gearman >= 0.5.0)

GearmanClient::doStatus — Отримання статусу завдання, що виконується

### Опис

```methodsynopsis
public GearmanClient::doStatus(): array
```

Повертає статус обробки запущеного завдання. Цей метод викликається між викликами, що повторюються. [GearmanClient::doNormal()](gearmanclient.donormal.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив, що становить відсоткове відношення виконаної роботи. Перший елемент відповідає кількості оброблених чанків, другий – загальна кількість даних.

### Приклади

**Приклад #1 Отримання стану виконання довгого завдання**

У цьому прикладі в обробник, що перевертає рядок, впроваджена затримка, щоб змоделювати завдання, що довго виконується. Після кожної паузи обробник виконує [GearmanJob::status()](gearmanjob.status.md)результат якого підхоплюється клієнтом.

```php
<?php

echo "Запуск\n";

# Создаём объект клиента.
$gmclient= new GearmanClient();

# Добавляем сервер по умолчанию (localhost).
$gmclient->addServer();

echo "Отправка задание\n";

# Отправляем задание перевернуть строку
do
{
  $result = $gmclient->doNormal("reverse", "Hello!");

  # Проверяем, есть ли ошибки или готовые данные.
  switch($gmclient->returnCode())
  {
    case GEARMAN_WORK_DATA:
      break;
    case GEARMAN_WORK_STATUS:
      # получить статус выполнения задания
      list($numerator, $denominator)= $gmclient->doStatus();
      echo "Статус: $numerator/$denominator завершено\n";
      break;
    case GEARMAN_WORK_FAIL:
      echo "Ошибка\n";
      exit;
    case GEARMAN_SUCCESS:
      break;
    default:
      echo "Код возврата: " . $gmclient->returnCode() . "\n";
      exit;
  }
}
while($gmclient->returnCode() != GEARMAN_SUCCESS);

echo "Успешно: $result\n";

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Запуск
Отправка задания
Состояние: 1/6 завершено
Состояние: 2/6 завершено
Состояние: 3/6 завершено
Состояние: 4/6 завершено
Состояние: 5/6 завершено
Состояние: 6/6 завершено
Успешно: !olleH
```

### Дивіться також

-   [GearmanClient::doNormal()](gearmanclient.donormal.md) - Виконує одиночне завдання та повертає результат
-   [GearmanJob::status()](gearmanjob.status.md) - Надсилання статусу завдання (застарілий метод)
