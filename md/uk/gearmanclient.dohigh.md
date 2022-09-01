---
navigation:
  - gearmanclient.dobackground.html: '« GearmanClient::doBackground'
  - gearmanclient.dohighbackground.html: 'GearmanClient::doHighBackground »'
  - index.html: PHP Manual
  - class.gearmanclient.html: GearmanClient
title: 'GearmanClient::doHigh'
---
# GearmanClient::doHigh

(PECL gearman >= 0.5.0)

GearmanClient::doHigh - Запускає на виконання завдання з високим пріоритетом

### Опис

```methodsynopsis
public GearmanClient::doHigh(string $function_name, string $workload, string $unique = ?): string
```

Запускає виконання одиночну високопріоритетну завдання і повертає рядок, що містить результат. Функція залежить від [GearmanClient](class.gearmanclient.html) і [GearmanWorker](class.gearmanworker.html)оскільки необхідно забезпечити єдиний формат результату. Високопріоритетні завдання мають перевагу над нормальними та низькопріоритетними завданнями у черзі завдань.

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

-   [GearmanClient::doNormal()](gearmanclient.donormal.html) - Виконує одиночне завдання та повертає результат
-   [GearmanClient::doLow()](gearmanclient.dolow.html) - Запускає виконання завдання з низьким пріоритетом
-   [GearmanClient::doBackground()](gearmanclient.dobackground.html) - Запускає виконання завдання у фоновому режимі
-   [GearmanClient::doHighBackground()](gearmanclient.dohighbackground.html) - Запускає на виконання із високим пріоритетом завдання у фоновому режимі
-   [GearmanClient::doLowBackground()](gearmanclient.dolowbackground.html) - Запускає на виконання з низьким пріоритетом завдання у фоновому режимі
