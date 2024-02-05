---
navigation:
  - gearmanclient.dolow.md: '« GearmanClient::doLow'
  - gearmanclient.donormal.md: 'GearmanClient::doNormal »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::doLowBackground'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanClient::doLowBackground

(PECL gearman >= 0.5.0)

GearmanClient::doLowBackground — Запускає на виконання з низьким пріоритетом завдання у фоновому режимі

### Опис

```methodsynopsis
public GearmanClient::doLowBackground(string $function, string $workload, ?string $unique = null): string
```

Запускає виконання з низьким пріоритетом завдання у фоновому режимі, повертаючи дескриптор завдання, який може бути використаний для запиту стану завдання, що виконується. Завдання нормального та високого пріоритету мають перевагу над низькопріоритетними завданнями у черзі завдань.

### Список параметрів

`function`

Зареєстрована функція, що викликається робочим процесом

`workload`

Серіалізовані дані, що підлягають обробці

`unique`

Унікальний ID, який призначається певному завданню

### Значення, що повертаються

Дескриптор відправленого завдання.

### Дивіться також

-   [GearmanClient::doNormal()](gearmanclient.donormal.md) \- Виконує одиночне завдання та повертає результат
-   [GearmanClient::doHigh()](gearmanclient.dohigh.md) \- Запускає на виконання завдання із високим пріоритетом
-   [GearmanClient::doLow()](gearmanclient.dolow.md) \- Запускає виконання завдання з низьким пріоритетом
-   [GearmanClient::doBackground()](gearmanclient.dobackground.md) \- Запускає виконання завдання у фоновому режимі
-   [GearmanClient::doHighBackground()](gearmanclient.dohighbackground.md) \- Запускає на виконання із високим пріоритетом завдання у фоновому режимі
