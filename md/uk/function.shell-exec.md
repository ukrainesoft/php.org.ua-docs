- [«proc_terminate](function.proc-terminate.md)
- [system »](function.system.md)

- [PHP Manual](index.md)
- [Функції запуску програм](ref.exec.md)
- Виконати команду через оболонку та повернути висновок у вигляді рядка

#shell_exec

(PHP 4, PHP 5, PHP 7, PHP 8)

shell_exec — Виконати команду через оболонку та повернути висновок у вигляді
рядки

### Опис

**shell_exec**(string `$command`): string\|false\|null

Функція ідентична оператору з [назад апострофом](language.operators.execution.md).

> **Примітка**:
>
> У Windows нижчий канал відкривається в текстовому режимі, що може
> привести до збою функції двійкового виведення. В такому випадку
> Спробуйте натомість використати [popen()](function.popen.md).

### Список параметрів

`command`
Команда, яка буде виконана.

### Значення, що повертаються

Рядок (string), що містить висновок виконаної команди, **`false`**, якщо
канал не може бути встановлений або **`null`** у разі виникнення
помилки або відсутність висновку команди.

> **Примітка**:
>
> Ця функція може повернути **`null`** у двох випадках: якщо відбулася
> помилка або якщо команда, що виконується, нічого не виводить. Не користуйтесь
> цією функцією, щоб визначити, чи успішно виконалася команда. Замість
> цього використовуйте [exec()](function.exec.md), оскільки вона
> дозволяє перевірити код повернення.

### Помилки

Видається помилка рівня **`E_WARNING`**, коли канал не може бути
встановлений.

### Приклади

**Приклад #1 Приклад використання **shell_exec()****

` <?php$output = shell_exec('ls -lart');echo "<pre>$output</pre>";?> `

### Дивіться також

- [exec()](function.exec.md) - Виконати зовнішню програму
- [escapeshellcmd()](function.escapeshellcmd.md) - Екранувати
метасимволи командного рядка
