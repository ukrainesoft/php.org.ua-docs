---
navigation:
  - function.escapeshellarg.md: « escapeshellarg
  - function.exec.md: exec »
  - index.md: PHP Manual
  - ref.exec.md: Функції запуску програм
title: escapeshellcmd
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# escapeshellcmd

(PHP 4, PHP 5, PHP 7, PHP 8)

escapeshellcmd — Екранувати метасимволи командного рядка

### Опис

```methodsynopsis
escapeshellcmd(string $command): string
```

Команда**escapeshellcmd()** екранує будь-які символи у рядку, які можуть бути використані для обману команди оболонки під час виконання довільних команд. Ця функція повинна бути використана, щоб переконатися, що будь-які дані, що вводяться користувачем, будуть екрановані перед передачею їх функцій [exec()](function.exec.md) або [system()](function.system.md) або оператору ["зворотний апостроф"](language.operators.execution.md)

Наступні символи будуть екрановані за допомогою зворотного слішу: ``&#;`|*?~<>^()[]{}$\`` `\x0A`и`\xFF`. Символи `'`и`"` екрануються тільки в тому випадку, якщо вони не попарно зустрічаються. У Windows все цим символам, плюс `!`и`%`предшествует символ каретки (`^`

### Список параметрів

`command`

Команда, яка буде екранована.

### Значення, що повертаються

Екранований рядок.

### Приклади

**Приклад #1 Приклад використання** escapeshellcmd()\*\*\*\*

```php
<?php
// Мы намеренно допускаем здесь произвольное количество аргументов.
$command = './configure '.$_POST['configure_options'];

$escaped_command = escapeshellcmd($command);

system($escaped_command);
?>
```

**Увага**

Функцию**escapeshellcmd()** слід використовувати над усім командним рядком, але вона все ще дозволяє атакуючому передати довільну кількість аргументів. Для екранування одного аргументу натомість необхідно використовувати функцію [escapeshellarg()](function.escapeshellarg.md)

**Увага**

Прогалини не будуть екрановані за допомогою **escapeshellcmd()**, що може бути проблематичним у Windows з такими шляхами, як: `C:\Program Files\ProgramName\program.exe`Можно уменьшить проблему, используя следующий фрагмент кода:

```php
<?php
$cmd = preg_replace('`(?<!^) `', '^ ', escapeshellcmd($cmd));
```

### Дивіться також

-   [escapeshellarg()](function.escapeshellarg.md) \- Екранувати рядок для того, щоб він міг бути використаний як аргумент командного рядка
-   [exec()](function.exec.md) \- Виконати зовнішню програму
-   [popen()](function.popen.md) \- Відкриває файловий покажчик процесу
-   [system()](function.system.md) \- Виконати зовнішню програму та відобразити висновок
-   [Оператор виконання](language.operators.execution.md)
