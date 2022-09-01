---
navigation:
  - gearmanclient.dohigh.md: '« GearmanClient::doHigh'
  - gearmanclient.dojobhandle.md: 'GearmanClient::doJobHandle »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::doHighBackground'
---
# GearmanClient::doHighBackground

(PECL gearman >= 0.5.0)

GearmanClient::doHighBackground — Запускає на виконання з високим пріоритетом завдання у фоновому режимі

### Опис

```methodsynopsis
public GearmanClient::doHighBackground(string $function_name, string $workload, string $unique = ?): string
```

Запускає виконання з високим пріоритетом завдання у фоновому режимі, повертаючи дескриптор завдання, який може бути надалі використаний для запиту стану завдання, що виконується. Завдання високого пріоритету мають перевагу над нормальними та низькопріоритетними завданнями у черзі завдань.

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

-   [GearmanClient::doNormal()](gearmanclient.donormal.md) - Виконує одиночне завдання та повертає результат
-   [GearmanClient::doHigh()](gearmanclient.dohigh.md) - Запускає на виконання завдання із високим пріоритетом
-   [GearmanClient::doLow()](gearmanclient.dolow.md) - Запускає виконання завдання з низьким пріоритетом
-   [GearmanClient::doBackground()](gearmanclient.dobackground.md) - Запускає виконання завдання у фоновому режимі
-   [GearmanClient::doLowBackground()](gearmanclient.dolowbackground.md) - Запускає на виконання з низьким пріоритетом завдання у фоновому режимі
