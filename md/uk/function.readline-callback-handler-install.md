---
navigation:
  - function.readline-add-history.md: « readline\_add\_history
  - function.readline-callback-handler-remove.md: readline\_callback\_handler\_remove »
  - index.md: PHP Manual
  - ref.readline.md: Опції Readline
title: readline\_callback\_handler\_install
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# readline\_callback\_handler\_install

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

readline\_callback\_handler\_install — Ініціалізує callback-інтерфейс readline та термінал, друкує рядок запрошення та негайно повертає керування

### Опис

```methodsynopsis
readline_callback_handler_install(string $prompt, callable $callback): bool
```

Ініціалізує callback-інтерфейс readline, друкує `prompt` та повертає управління. Повторний виклик цієї функції без попереднього видалення старого callback-інтерфейсу призведе до його автоматичного перезапису.

Функціонал callback-функцій особливо зручний у комбінації з [stream\_select()](function.stream-select.md), оскільки він, на відміну від [readline()](function.readline.md), дозволяє чергувати введення-виведення та введення користувача.

### Список параметрів

`prompt`

Рядок запрошення.

`callback`

Функция передаваемая в параметр`callback` повинна приймати один параметр - повернутий введення користувача.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання callback-інтерфейсу readline**

```php
<?php
function rl_callback($ret)
{
    global $c, $prompting;

    echo "Вы ввели: $ret\n";
    $c++;

    if ($c > 10) {
        $prompting = false;
        readline_callback_handler_remove();
    } else {
        readline_callback_handler_install("[$c] Поговори со мной: ", 'rl_callback');
    }
}

$c = 1;
$prompting = true;

readline_callback_handler_install("[$c] Введите что-нибудь: ", 'rl_callback');

while ($prompting) {
    $w = NULL;
    $e = NULL;
    $n = stream_select($r = array(STDIN), $w, $e, null);
    if ($n && in_array(STDIN, $r)) {
        // читаем символ и вызываем callback-функцию,
        // если введён символ новой строки
        readline_callback_read_char();
    }
}

echo "Ввод отключён. Спасибо за внимание.\n";
?>
```

### Дивіться також

-   [readline\_callback\_handler\_remove()](function.readline-callback-handler-remove.md) \- Видаляє раніше зареєстровану callback-функцію та відновлює термінал
-   [readline\_callback\_read\_char()](function.readline-callback-read-char.md) \- Читає символ та інформує callback-функцію readline, що отримано рядок
-   [stream\_select()](function.stream-select.md) \- Запускає еквівалент системного виклику select() на заданих масивах потоків з часом очікування, вказаним параметрами seconds та microseconds
