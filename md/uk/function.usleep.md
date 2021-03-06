- [«unpack](function.unpack.md)
- [Список змін »](changelog.misc.md)

- [PHP Manual](index.md)
- [Різні функції](ref.misc.md)
- Затримка виконання у мікросекундах

# usleep

(PHP 4, PHP 5, PHP 7, PHP 8)

usleep — Затримка виконання у мікросекундах

### Опис

**usleep**(int `$microseconds`): void

Відкладає виконання програми на вказану кількість мікросекунд.

### Список параметрів

`microseconds`
Час виконання, що відкладається в мікросекундах. Мікросекунда – це одна
мільйонні секунди.

> **Примітка**: Значення більше `1000000` (тобто очікування більше секунди)
> можуть не підтримуватись операційною системою. Замість цього
> використовуйте [sleep()](function.sleep.md).

> **Примітка**: У Windows система може відкладати виконання довше
> вказаної кількості мікросекунд, залежно від апаратного
> Забезпечення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **usleep()****

` <?php// Поточний часecho date('h:i:s') . "
";// ждати 2 секундиusleep(2000000);// повернутися до виконанняecho date('h:i:s') . ""
";?> `

Результат виконання цього прикладу:

11:13:28
11:13:30

### Дивіться також

- [sleep()](function.sleep.md) - Затримка виконання
- [time_nanosleep()](function.time-nanosleep.md) - Затримка на
задане число секунд і наносекунд
- [time_sleep_until()](function.time-sleep-until.md) - Відкладає
виконання скрипту до заданого часу
- [set_time_limit()](function.set-time-limit.md) - Обмеження
часу виконання скрипту
