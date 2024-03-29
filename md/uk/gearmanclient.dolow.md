---
navigation:
  - gearmanclient.dojobhandle.md: '« GearmanClient::doJobHandle'
  - gearmanclient.dolowbackground.md: 'GearmanClient::doLowBackground »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::doLow'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanClient::doLow

(PECL gearman >= 0.5.0)

GearmanClient::doLow - Запускає на виконання завдання з низьким пріоритетом

### Опис

```methodsynopsis
public GearmanClient::doLow(string $function, string $workload, ?string $unique = null): string
```

Запускає виконання завдання з низьким пріоритетом і повертає рядок, що містить результат. Функція залежить від [GearmanClient](class.gearmanclient.md) і [GearmanWorker](class.gearmanworker.md)оскільки необхідно забезпечити єдиний формат результату. Високопріоритетні завдання мають перевагу над звичайними та низькопріоритетними завданнями у черзі завдань. Завдання нормального та високого пріоритету мають перевагу над низькопріоритетними завданнями у черзі завдань.

### Список параметрів

`function`

Зареєстрована функція, що викликається робочим процесом

`workload`

Серіалізовані дані, що підлягають обробці

`unique`

Унікальний ID, який призначається певному завданню

### Значення, що повертаються

Рядок, що містить результат виконання завдання.

### Дивіться також

-   [GearmanClient::doNormal()](gearmanclient.donormal.md) \- Виконує одиночне завдання та повертає результат
-   [GearmanClient::doHigh()](gearmanclient.dohigh.md) \- Запускає на виконання завдання із високим пріоритетом
-   [GearmanClient::doBackground()](gearmanclient.dobackground.md) \- Запускає виконання завдання у фоновому режимі
-   [GearmanClient::doHighBackground()](gearmanclient.dohighbackground.md) \- Запускає на виконання із високим пріоритетом завдання у фоновому режимі
-   [GearmanClient::doLowBackground()](gearmanclient.dolowbackground.md) \- Запускає на виконання з низьким пріоритетом завдання у фоновому режимі
