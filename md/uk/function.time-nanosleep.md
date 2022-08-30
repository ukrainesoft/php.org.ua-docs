Затримка на задану кількість секунд та наносекунд

-   [« sysgetloadavg](function.sys-getloadavg.html)
    
-   [timesleepuntil »](function.time-sleep-until.html)
    
-   [PHP Manual](index.md)
    
-   [Різні функції](ref.misc.md)
    
-   Затримка на задану кількість секунд та наносекунд
    

# timenanosleep

(PHP 5, PHP 7, PHP 8)

timenanosleep — Затримка на задану кількість секунд та наносекунд

### Опис

```methodsynopsis
time_nanosleep(int $seconds, int $nanoseconds): array|bool
```

Відкладає виконання програми на задані параметри `seconds` і `nanoseconds` число секунд та наносекунд відповідно.

### Список параметрів

`seconds`

Має бути цілим позитивним числом.

`nanoseconds`

Має бути цілим позитивним числом, меншим за один мільярд.

> **Зауваження**: У Windows система може відкладати виконання довше зазначеної кількості наносекунд, залежно від апаратного забезпечення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

Якщо відкладене виконання було перервано сигналом, повертається асоціативний масив з наступними компонентами:

-   `seconds` - кількість секунд, що залишилися
-   `nanoseconds` - кількість наносекунд, що залишилися

### Приклади

**Приклад #1 Приклад використання **timenanosleep()****

```php
<?php
// Внимание! Если будет возвращён Масив, то такая функция не сработает, как ожидалось
if (time_nanosleep(0, 500000000)) {
    echo "Задержка на полсекунды.\n";
}

// Так лучше:
if (time_nanosleep(0, 500000000) === true) {
    echo "Задержка на полсекунды.\n";
}

// А так лучше всего:
$nano = time_nanosleep(2, 100000);

if ($nano === true) {
    echo "Задержка на 2 секунды, 100 микросекунд.\n";
} elseif ($nano === false) {
    echo "Задержка не удалась.\n";
} elseif (is_array($nano)) {
    $seconds = $nano['seconds'];
    $nanoseconds = $nano['nanoseconds'];
    echo "Прервано сигналом.\n";
    echo "Осталось: $seconds секунд, $nanoseconds наносекунд.";
}
?>
```

### Дивіться також

-   [sleep()](function.sleep.md) - затримка виконання
-   [usleep()](function.usleep.md) - Затримка виконання у мікросекундах
-   [timesleepuntil()](function.time-sleep-until.html) - Відкладає виконання скрипту до заданого часу
-   [settimelimit()](function.set-time-limit.html) - Обмеження часу виконання скрипту