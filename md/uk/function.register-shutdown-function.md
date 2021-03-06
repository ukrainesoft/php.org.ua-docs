- [«get_defined_functions](function.get-defined-functions.md)
- [register_tick_function »](function.register-tick-function.md)

- [PHP Manual](index.md)
- [Функції керування функціями](ref.funchand.md)
- реєструє функцію, яка виконається при завершенні роботи
скрипта

# register_shutdown_function

(PHP 4, PHP 5, PHP 7, PHP 8)

register_shutdown_function — Реєструє функцію, що виконається
після завершення роботи скрипта

### Опис

**register_shutdown_function**([callable](language.types.callable.md)
`$callback`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`...$args`): ?bool

Реєструє функцію callback, яка виконається після завершення
роботи скрипта або під час виклику функції [exit()](function.exit.md).

Можлива реєстрація кількох подібних функцій за допомогою
**register_shutdown_function()**, при цьому функції будуть виконуватись у
порядку, в якому вони були зареєстровані. Якщо ви викличете
[exit()](function.exit.md) в одній із зареєстрованих завершальних
функцій, процес буде повністю зупинено та наступні завершальні
функції не будуть викликані.

Завершальні функції також можуть викликати самі
**register_shutdown_function()**, щоб додати функцію вимкнення в
кінець черги.

### Список параметрів

`callback`
Реєструється завершальна функція.

Завершальні функції виконуються як частина запиту, тому можна
надсилати дані на виведення з них та отримувати доступ до буферизації
виведення.

`args`
Можна передавати параметри на завершальну функцію, передавши додаткові
параметри.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Якщо передано назву неіснуючої завершальної функції, то
генерується помилка рівня **`E_WARNING`**.

### Приклади

**Приклад #1 Приклад використання **register_shutdown_function()****

` <?phpfunction shutdown(){    // Це наша завершальна функція,    // тут ми можемо виконати всі останні операції завершення//  echo 'Скрипт успішно закінчився', PHP_EOL;}register_shutdown_function('shutdown');?> `

### Примітки

> **Примітка**:
>
> Робоча директорія скрипта може змінитися всередині завершальної функції
> деякі веб-сервери, наприклад, Apache.

> **Примітка**:
>
> Функції, які виконуються після завершення скрипта, не будуть виконані, якщо
> процес був убитий із сигналами SIGTERM або SIGKILL. Хоча ви й не можете
> перехопити SIGKILL, але можна використовувати функцію
> [pcntl_signal()](function.pcntl-signal.md), щоб поставити обробник
> сигналу SIGTERM, який використовує функцію
> [exit()](function.exit.md), щоб завершити скрипт правильно.

> **Примітка**:
>
> Завершальні функції виконуються окремо від часу, відстежуваного
> [max_execution_time](info.configuration.md#ini.max-execution-time).
> Це означає, що навіть якщо процес буде завершено через занадто
> довготривалого виконання, завершальні функції все одно будуть викликані. Крім
> того, якщо `max_execution_time` закінчиться під час роботи завершальної
> функції, процес не буде завершено.

### Дивіться також

- [auto_append_file](ini.core.md#ini.auto-append-file)
- [exit()](function.exit.md) - Вивести повідомлення та припинити
виконання поточного скрипту
- [fastcgi_finish_request()](function.fastcgi-finish-request.md) -
скидає всі запитані дані клієнту
- Розділ [Обробка з'єднань](features.connection-handling.md)
