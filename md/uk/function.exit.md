---
navigation:
  - function.eval.md: « eval
  - function.get-browser.md: get\_browser »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: exit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# exit

(PHP 4, PHP 5, PHP 7, PHP 8)

exit — Виводить повідомлення та припиняє виконання поточного скрипту

### Опис

```methodsynopsis
exit(string $status = ?): void
```

```methodsynopsis
exit(int $status): void
```

Припиняє виконання скрипту . [Функції відключення](function.register-shutdown-function.md) і [деструктори об'єкту](language.oop5.decon.md#language.oop5.decon.destructor) будуть запущені, навіть якщо було викликано конструкцію `exit`

`exit` - це конструкція мови, і вона може бути викликана без круглих дужок, якщо не передається параметр `status`

### Список параметрів

`status`

Якщо `status` заданий у вигляді рядка, то ця конструкція виведе вміст `status` перед виходом.

Якщо `status` заданий у вигляді цілого числа (int), це значення буде використано як статус виходу і буде виведено. Статуси виходу повинні бути в діапазоні від 0 до 254, статус виходу 255 зарезервований PHP і не використовується. Статус виходу 0 вказують на успішне завершення програми.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання мовної конструкції `exit`**

```php
<?php

$filename = '/path/to/data-file';
$file = fopen($filename, 'r')
    or exit("Невозможно открыть файл ($filename)");

?>
```

**Приклад #2 Приклад використання конструкції `exit` зі статусом виходу**

```php
<?php

// обычный выход из программы
exit;
exit();
exit(0);

// выход с кодом ошибки
exit(1);
exit(0376); // восьмеричный

?>
```

**Приклад #3 Функції вимкнення та деструктори виконуються незалежно**

```php
<?php
class Foo
{
    public function __destruct()
    {
        echo 'Деинициализировать: ' . __METHOD__ . '()' . PHP_EOL;
    }
}

function shutdown()
{
    echo 'Завершить: ' . __FUNCTION__ . '()' . PHP_EOL;
}

$foo = new Foo();
register_shutdown_function('shutdown');

exit();
echo 'Эта строка не будет выведена.';
?>
```

Результат виконання наведеного прикладу:

```
Завершить: shutdown()
 Деинициализировать: Foo::__destruct()
```

### Примітки

> **Зауваження**: Оскільки це мовна конструкція, а не функція, її не можна викликати як [змінну функцію](functions.variable-functions.md) або передавати як [іменований аргумент](functions.arguments.md#functions.named-arguments)

> **Зауваження** :
> 
> Ця мовна конструкція еквівалентна конструкції [die()](function.die.md)

### Дивіться також

-   [register\_shutdown\_function()](function.register-shutdown-function.md) \- Реєструє функцію, яка виконається після завершення роботи скрипту
