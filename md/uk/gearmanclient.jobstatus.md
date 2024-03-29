---
navigation:
  - gearmanclient.geterrno.md: '« GearmanClient::getErrno'
  - gearmanclient.ping.md: 'GearmanClient::ping »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::jobStatus'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanClient::jobStatus

# gearman\_job\_status

(PECL gearman >= 0.5.0)

GearmanClient::jobStatus -- gearman\_job\_status — отримання статусу виконання фонового завдання

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public GearmanClient::jobStatus(string $job_handle): array
```

Отримує стан виконання завдання, запущеного у фоновому режимі. Інформація про стан включає дані про те, що завдання відомо обробнику, чи виконується завдання в даний момент, а також відсоток оброблених даних.

### Список параметрів

`job_handle`

Дескриптор завдання, який надається сервером Gearman

### Значення, що повертаються

Масив, що містить інформацію про завдання, яке відповідає заданому дескриптору завдання. Перший елемент масиву вказує, чи обробник знає про це завдання. Другий елемент вказує, чи виконується завдання на даний момент. Третій та четвертий елементи відповідають за частку виконаної роботи та загальний обсяг даних, відповідно.

### Приклади

**Приклад #1 Моніторинг процесу обробки завдання, що довго виконується у фоновому режимі**

```php
<?php

/* создаём клиента */
$gmclient= new GearmanClient();

/* добавляем сервер по умолчанию */
$gmclient->addServer();

/* запускаем клиент */
$job_handle = $gmclient->doBackground("reverse", "this is a test");

if ($gmclient->returnCode() != GEARMAN_SUCCESS)
{
  echo "Не удалось выполнить задание\n";
  exit;
}

$done = false;
do
{
   sleep(3);
   $stat = $gmclient->jobStatus($job_handle);
   if (!$stat[0]) // задание известно обработчику, но ещё не завершено
      $done = true;
   echo "Выполняется: " . ($stat[1] ? "true" : "false") . ", обработано: " . $stat[2] . ", всего: " . $stat[3] . "\n";
}
while(!$done);

echo "завершено!\n";

?>
```

Висновок наведеного прикладу буде схожим на:

```
Выполняется: true, обработано: 3, всего: 14
Выполняется: true, обработано: 6, всего: 14
Выполняется: true, обработано: 9, всего: 14
Выполняется: true, обработано: 12, всего: 14
Выполняется: false, обработано: 0, всего: 0
завершено!
```

### Дивіться також

-   [GearmanClient::doStatus()](gearmanclient.dostatus.md) \- Отримання статусу завдання, що виконується
