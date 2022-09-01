---
navigation:
  - gearmanclient.dolow.html: '« GearmanClient::doLow'
  - gearmanclient.donormal.html: 'GearmanClient::doNormal »'
  - index.html: PHP Manual
  - class.gearmanclient.html: GearmanClient
title: 'GearmanClient::doLowBackground'
---
# GearmanClient::doLowBackground

(PECL gearman >= 0.5.0)

GearmanClient::doLowBackground — Запускає на виконання з низьким пріоритетом завдання у фоновому режимі

### Опис

```methodsynopsis
public GearmanClient::doLowBackground(string $function_name, string $workload, string $unique = ?): string
```

Запускає виконання з низьким пріоритетом завдання у фоновому режимі, повертаючи дескриптор завдання, який може бути використаний для запиту стану завдання, що виконується. Завдання нормального та високого пріоритету мають перевагу над низькопріоритетними завданнями у черзі завдань.

### Список параметрів

`function_name`

Зареєстрована функція, що викликається робочим процесом

`workload`

Серіалізовані дані, що підлягають обробці

`unique`

Унікальний ID, який призначається певному завданню

### Значення, що повертаються

Дескриптор відправленого завдання.

### Дивіться також

-   [GearmanClient::doNormal()](gearmanclient.donormal.html) - Виконує одиночне завдання та повертає результат
-   [GearmanClient::doHigh()](gearmanclient.dohigh.html) - Запускає на виконання завдання із високим пріоритетом
-   [GearmanClient::doLow()](gearmanclient.dolow.html) - Запускає виконання завдання з низьким пріоритетом
-   [GearmanClient::doBackground()](gearmanclient.dobackground.html) - Запускає виконання завдання у фоновому режимі
-   [GearmanClient::doHighBackground()](gearmanclient.dohighbackground.html) - Запускає на виконання із високим пріоритетом завдання у фоновому режимі
