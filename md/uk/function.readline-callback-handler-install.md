Ініціалізує callback-інтерфейс readline та термінал, друкує рядок запрошення та негайно повертає управління

-   [« readlineaddhistory](function.readline-add-history.html)
    
-   [readlinecallbackhandlerremove »](function.readline-callback-handler-remove.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Readline](ref.readline.html)
    
-   Ініціалізує callback-інтерфейс readline та термінал, друкує рядок запрошення та негайно повертає управління
    

# readlinecallbackhandlerinstall

(PHP 5> = 5.1.0, PHP 7, PHP 8)

readlinecallbackhandlerinstall — Ініціалізує callback-інтерфейс readline та термінал, друкує рядок запрошення та негайно повертає керування

### Опис

```methodsynopsis
readline_callback_handler_install(string $prompt, callable $callback): bool
```

Ініціалізує callback-інтерфейс readline, друкує `prompt` та повертає управління. Повторний виклик цієї функції без попереднього видалення старого callback-інтерфейсу призведе до його автоматичного перезапису.

Функціонал callback-функцій особливо зручний у комбінації з [streamselect()](function.stream-select.html), оскільки він, на відміну від [readline()](function.readline.html), дозволяє чергувати введення-виведення та введення користувача.

### Список параметрів

`prompt`

Рядок запрошення.

`callback`

Функція, що передається в параметр `callback` повинна приймати один параметр - повернутий введення користувача.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання callback-інтерфейсу readline**

```php
<?php
function rl_callback($ret)
{
    global $c, $prompting;

    echo "Вы ввели: $ret\n";
    $c++;

    if ($c > 10) {
        $prompting = false;
        readline_callback_handler_remove();
    } else {
        readline_callback_handler_install("[$c] Поговори со мной: ", 'rl_callback');
    }
}

$c = 1;
$prompting = true;

readline_callback_handler_install("[$c] Введите что-нибудь: ", 'rl_callback');

while ($prompting) {
    $w = NULL;
    $e = NULL;
    $n = stream_select($r = array(STDIN), $w, $e, null);
    if ($n && in_array(STDIN, $r)) {
        // читаем символ и вызываем callback-функцию,
        // если введён символ новой строки
        readline_callback_read_char();
    }
}

echo "Ввод отключён. Спасибо за внимание.\n";
?>
```

### Дивіться також

-   [readlinecallbackhandlerremove()](function.readline-callback-handler-remove.html) - Видаляє раніше зареєстровану callback-функцію та відновлює термінал
-   [readlinecallbackreadchar()](function.readline-callback-read-char.html) - Читає символ та інформує callback-функцію readline, що отримано рядок
-   [streamselect()](function.stream-select.html) - Запускає еквівалент системного виклику select() на заданих масивах потоків з часом очікування, вказаним параметрами seconds та microseconds