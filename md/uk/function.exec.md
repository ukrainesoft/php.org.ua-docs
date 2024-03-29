---
navigation:
  - function.escapeshellcmd.md: « escapeshellcmd
  - function.passthru.md: passthru »
  - index.md: PHP Manual
  - ref.exec.md: Функції запуску програм
title: exec
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# exec

(PHP 4, PHP 5, PHP 7, PHP 8)

exec — Виконати зовнішню програму

### Опис

```methodsynopsis
exec(string $command, array &$output = null, int &$result_code = null): string|false
```

**exec()** виконує команду `command`

### Список параметрів

`command`

Команда, яка буде виконана.

`output`

Якщо параметр `output` вказано, що масив буде заповнений рядками виведення програми. Завершальні прогалини, такі як `\n`, не будуть включені до масиву. Зверніть увагу, що якщо масив вже містить якісь елементи, то **exec()** додасть нові елементи до кінця масиву. Якщо ви не бажаєте, щоб функція додавала нові елементи в кінець, викличте [unset()](function.unset.md) на цьому масиві, перш ніж передати його в **exec()**

`result_code`

Якщо аргумент `result_code` присутній разом з `output`, Тоді статус повернення виконаної команди буде записаний у цій змінній.

### Значення, що повертаються

Останній рядок із результату команди. Якщо потрібно виконати команду та отримати всі дані команди без будь-якої обробки, використовуйте функцію [passthru()](function.passthru.md)

Повертає \*\*`false`\*\*в случае возникновения ошибки.

Щоб отримати результат виконання команди, переконайтеся, що параметр `output` ініціалізований та використовується.

### Помилки

Видає помилку рівня **`E_WARNING`**, якщо функція **exec()** не може виконати команду `command`

Викидає виняток [ValueError](class.valueerror.md), якщо параметр `command` не вказано або містить нульові байти.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Якщо параметр `command` не вказано або містить нульові байти, функція **exec()** тепер викидає виняток [ValueError](class.valueerror.md); раніше вона видавала помилку рівня **`E_WARNING`** і повертала **`false`** |

### Приклади

**Приклад #1 Приклад функції **exec()****

```php
<?php
// выводит имя пользователя, от имени которого запущен процесс php/httpd
// (применимо к системам с командой "whoami" в системном пути)
$output=null;
$retval=null;
exec('whoami', $output, $retval);
echo "Вернёт статус $retval и значение:\n";
print_r($output);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Вернёт статус 0 и значение:
Array
(
    [0] => cmb
)
```

### Примітки

**Увага**

Якщо потрібно передавати функції дані користувача, викликають функції [escapeshellarg()](function.escapeshellarg.md) або [escapeshellcmd()](function.escapeshellcmd.md)щоб користувачі не змогли обдурити систему, запустивши довільну команду.

> **Зауваження** :
> 
> Якщо потрібно викликати цю функцію в програмі, що працює як демон, перевіряють, що стандартне виведення функції направлено у файл або інший потік, інакше PHP зависне аж до кінця виконання програми.

> **Зауваження** :
> 
> В Windows функция**exec()** Запуск команди запускає командний рядок cmd.exe. Якщо потрібно запустити зовнішню програму без запуску командного рядка cmd.exe, викликають функцію [proc\_open()](function.proc-open.md) із встановленою опцією `bypass_shell`

### Дивіться також

-   [system()](function.system.md) \- Виконати зовнішню програму та відобразити висновок
-   [passthru()](function.passthru.md) \- Виконати зовнішню програму та відобразити необроблений висновок
-   [escapeshellcmd()](function.escapeshellcmd.md) \- Екранувати метасимволи командного рядка
-   [pcntl\_exec()](function.pcntl-exec.md) \- Запустити вказану програму в галузі поточного процесу
-   [Оператор виконання](language.operators.execution.md)
