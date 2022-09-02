---
navigation:
  - gearmanclient.dobackground.md: '« GearmanClient::doBackground'
  - gearmanclient.dohighbackground.md: 'GearmanClient::doHighBackground »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::doHigh'
---
# GearmanClient::doHigh

(PECL gearman >= 0.5.0)

GearmanClient::doHigh - Запускає на виконання завдання з високим пріоритетом

### Опис

```methodsynopsis
public GearmanClient::doHigh(string $function_name, string $workload, string $unique = ?): string
```

Запускає виконання одиночну високопріоритетну завдання і повертає рядок, що містить результат. Функція залежить від [GearmanClient](class.gearmanclient.md) і [GearmanWorker](class.gearmanworker.md)оскільки необхідно забезпечити єдиний формат результату. Високопріоритетні завдання мають перевагу над нормальними та низькопріоритетними завданнями у черзі завдань.

### Список параметрів

`function_name`

Зареєстрована функція, що викликається робочим процесом

`workload`

Серіалізовані дані, що підлягають обробці

`unique`

Унікальний ID, який призначається певному завданню

### Значення, що повертаються

Рядок, що містить результат виконання завдання.

### Дивіться також

-   [GearmanClient::doNormal()](gearmanclient.donormal.md) - Виконує одиночне завдання та повертає результат
-   [GearmanClient::doLow()](gearmanclient.dolow.md) - Запускає виконання завдання з низьким пріоритетом
-   [GearmanClient::doBackground()](gearmanclient.dobackground.md) - Запускає виконання завдання у фоновому режимі
-   [GearmanClient::doHighBackground()](gearmanclient.dohighbackground.md) - Запускає на виконання із високим пріоритетом завдання у фоновому режимі
-   [GearmanClient::doLowBackground()](gearmanclient.dolowbackground.md) - Запускає на виконання з низьким пріоритетом завдання у фоновому режимі
