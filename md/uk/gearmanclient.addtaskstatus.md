---
navigation:
  - gearmanclient.addtasklowbackground.html: '« GearmanClient::addTaskLowBackground'
  - gearmanclient.clearcallbacks.html: 'GearmanClient::clearCallbacks »'
  - index.html: PHP Manual
  - class.gearmanclient.html: GearmanClient
title: 'GearmanClient::addTaskStatus'
---
# GearmanClient::addTaskStatus

(PECL gearman >= 0.5.0)

GearmanClient::addTaskStatus — Додати завдання для отримання статусу

### Опис

```methodsynopsis
public GearmanClient::addTaskStatus(string $job_handle, string &$context = ?): GearmanTask
```

Використовується для запиту інформації про стан із сервера Gearman, який буде викликати вказаний callback-функцію статусу (задану через [GearmanClient::setStatusCallback()](gearmanclient.setstatuscallback.md)

### Список параметрів

`job_handle`

Дескриптор завдання для набуття статусу завдання

`context`

Дані, які будуть надіслані зворотному виклику. Зазвичай посилання на масив чи об'єкт

### Значення, що повертаються

Об'єкт [GearmanTask](class.gearmantask.md)

### Приклади

**Приклад #1 Моніторинг завершення кількох фонових завдань**

У цьому прикладі представлено штучну затримку в обробнику, щоб змоделювати тривалий робочий процес. Існує лише один обробник, запущений для цього прикладу.

```php
<?php

/* создание клиентского объекта */
$gmclient= new GearmanClient();

/* добавление сервера задач по умолчанию */
$gmclient->addServer();

/* запуск некоторых фоновых задач и сохранение дескрипторов */
$handles = array();
$handles[0] = $gmclient->doBackground("reverse", "Hello World!");
$handles[1] = $gmclient->doBackground("reverse", "!dlroW olleH");

$gmclient->setStatusCallback("reverse_status");

/* Опрос сервера с целью определения, когда завершатся фоновые задачи; */
/* лучшим методом может быть установка callback-функций на события */
do
{
   /* используем контекстные переменные для отслеживания за тем, сколько задач выполнилось */
   $done = 0;
   $gmclient->addTaskStatus($handles[0], &$done);
   $gmclient->addTaskStatus($handles[1], &$done);
   $gmclient->runTasks();
   echo "Выполнено: $done\n";
   sleep(1);
}
while ($done != 2);

function reverse_status($task, $done)
{
   if (!$task->isKnown())
      $done++;
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Выполнено: 0
Выполнено: 0
Выполнено: 0
Выполнено: 0
Выполнено: 0
Выполнено: 0
Выполнено: 0
Выполнено: 0
Выполнено: 0
Выполнено: 0
Выполнено: 0
Выполнено: 0
Выполнено: 1
Выполнено: 1
Выполнено: 1
Выполнено: 1
Выполнено: 1
Выполнено: 1
Выполнено: 1
Выполнено: 1
Выполнено: 1
Выполнено: 1
Выполнено: 1
Выполнено: 1
Выполнено: 2
```

### Дивіться також

-   [GearmanClient::setStatusCallback()](gearmanclient.setstatuscallback.md) - завдання callback-функції, що збирає інформацію про стан обробника завдань
