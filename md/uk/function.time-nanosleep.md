---
navigation:
  - function.sys-getloadavg.md: « sys\_getloadavg
  - function.time-sleep-until.md: time\_sleep\_until »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: time\_nanosleep
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# time\_nanosleep

(PHP 5, PHP 7, PHP 8)

time\_nanosleep — Затримка на задану кількість секунд і наносекунд

### Опис

```methodsynopsis
time_nanosleep(int $seconds, int $nanoseconds): array|bool
```

Відкладає виконання програми на задані параметри `seconds`и`nanoseconds` число секунд та наносекунд відповідно.

### Список параметрів

`seconds`

Має бути цілим позитивним числом.

`nanoseconds`

Має бути цілим позитивним числом, меншим за один мільярд.

> **Зауваження**: У Windows система може відкладати виконання довше зазначеної кількості наносекунд, залежно від апаратного забезпечення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

Якщо відкладене виконання було перервано сигналом, повертається асоціативний масив з наступними компонентами:

-   `seconds`\- кількість секунд, що залишилися
-   `nanoseconds`\- кількість наносекунд, що залишилися

### Приклади

**Приклад #1 Приклад використання** time\_nanosleep()\*\*\*\*

```php
<?php
// Внимание! Если будет возвращён массив, то такая функция не сработает, как ожидалось
if (time_nanosleep(0, 500000000)) {
    echo "Задержка на полсекунды.\n";
}

// Так лучше:
if (time_nanosleep(0, 500000000) === true) {
    echo "Задержка на полсекунды.\n";
}

// А так лучше всего:
$nano = time_nanosleep(2, 100000);

if ($nano === true) {
    echo "Задержка на 2 секунды, 100 микросекунд.\n";
} elseif ($nano === false) {
    echo "Задержка не удалась.\n";
} elseif (is_array($nano)) {
    $seconds = $nano['seconds'];
    $nanoseconds = $nano['nanoseconds'];
    echo "Прервано сигналом.\n";
    echo "Осталось: $seconds секунд, $nanoseconds наносекунд.";
}
?>
```

### Дивіться також

-   [sleep()](function.sleep.md) \- затримка виконання
-   [usleep()](function.usleep.md) \- Затримка виконання у мікросекундах
-   [time\_sleep\_until()](function.time-sleep-until.md) \- Відкладає виконання скрипту до заданого часу
-   [set\_time\_limit()](function.set-time-limit.md) \- Обмеження часу виконання скрипту
