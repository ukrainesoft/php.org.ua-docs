---
navigation:
  - ref.pcntl.md: « Функції PCNTL
  - function.pcntl-async-signals.md: pcntl\_async\_signals »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntl\_alarm
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pcntl\_alarm

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

pcntl\_alarm — Встановити таймер доставки сигналу SIGALRM

### Опис

```methodsynopsis
pcntl_alarm(int $seconds): int
```

Створює таймер, який надішле сигнал **`SIGALRM`** процесу через задану кількість секунд. Будь-який виклик функції **pcntl\_alarm()** скасує будь-який раніше заданий таймер.

### Список параметрів

`seconds`

Число секунд ожидания. Если в аргумент`seconds` переданий нуль, то новий таймер створено не буде.

### Значення, що повертаються

Повертає час у секундах, який залишався будь-якому попередньому таймеру для доставки сигналу, або поверне якщо раніше таймер не був заданий.
