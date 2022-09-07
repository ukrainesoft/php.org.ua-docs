---
navigation:
  - gearmanclient.do.md: '« GearmanClient::do'
  - gearmanclient.dohigh.md: 'GearmanClient::doHigh »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::doBackground'
---
# GearmanClient::doBackground

(PECL gearman >= 0.5.0)

GearmanClient::doBackground — Запуск виконання завдання у фоновому режимі

### Опис

```methodsynopsis
public GearmanClient::doBackground(string $function_name, string $workload, string $unique = ?): string
```

Запуск виконання завдання у фоновому режимі, повертаючи дескриптор завдання, який може бути використаний для запиту стану завдання, що виконується.

### Список параметрів

`function_name`

Зареєстрована функція, що викликається робочим процесом

`workload`

Серіалізовані дані, що підлягають обробці

`unique`

Унікальний ID, який призначається певному завданню

### Значення, що повертаються

Дескриптор завдання для надісланого завдання.

### Приклади

**Приклад #1 Відправляє та відстежує фонове завдання**

Оброблювач у цьому прикладі має штучну затримку, щоб змоделювати тривале виконання завдання. Клієнт періодично перевіряє стан завдання, що виконується.

```php
<?php

/* создание объекта */
$gmclient= new GearmanClient();

/* указание сервера по умолчанию */
$gmclient->addServer();

/* запуск выполнение клиента */
$job_handle = $gmclient->doBackground("reverse", "this is a test");

if ($gmclient->returnCode() != GEARMAN_SUCCESS)
{
  echo "неуспешный код возврата\n";
  exit;
}

$done = false;
do
{
   sleep(3);
   $stat = $gmclient->jobStatus($job_handle);
   if (!$stat[0]) // задание известно, но не выполнено
      $done = true;
   echo "Выполняется: " . ($stat[1] ? "true" : "false") . ", числитель: " . $stat[2] . ", знаменатель: " . $stat[3] . "\n";
}
while(!$done);

echo "завершено!\n";

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Выполняется: true, числитель: 3, знаменатель: 14
Выполняется: true, числитель: 6, знаменатель: 14
Выполняется: true, числитель: 9, знаменатель: 14
Выполняется: true, числитель: 12, знаменатель: 14
Выполняется: false, числитель: 0, знаменатель: 0
завершено!
```

### Дивіться також

-   [GearmanClient::doNormal()](gearmanclient.donormal.md) - Виконує одиночне завдання та повертає результат
-   [GearmanClient::doHigh()](gearmanclient.dohigh.md) - Запускає на виконання завдання із високим пріоритетом
-   [GearmanClient::doLow()](gearmanclient.dolow.md) - Запускає виконання завдання з низьким пріоритетом
-   [GearmanClient::doHighBackground()](gearmanclient.dohighbackground.md) - Запускає на виконання із високим пріоритетом завдання у фоновому режимі
-   [GearmanClient::doLowBackground()](gearmanclient.dolowbackground.md) - Запускає на виконання з низьким пріоритетом завдання у фоновому режимі
