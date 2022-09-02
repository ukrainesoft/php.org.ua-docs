---
navigation:
  - function.preg-replace-callback-array.md: « pregreplacecallbackarray
  - function.preg-replace.md: pregreplace »
  - index.md: PHP Manual
  - ref.pcre.md: Функции PCRE
title: pregreplacecallback
---
# pregreplacecallback

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

pregreplacecallback — Виконує пошук за регулярним виразом та заміною з використанням callback-функції

### Опис

```methodsynopsis
preg_replace_callback(    string|array $pattern,    callable $callback,    string|array $subject,    int $limit = -1,    int &$count = null,    int $flags = 0): string|array|null
```

Поведінка цієї функції багато в чому нагадує [pregreplace()](function.preg-replace.md), за винятком того, що замість параметра `replacement` необхідно вказувати `callback`функцію.

### Список параметрів

`pattern`

Шуканий шаблон. Можливо як рядком, і масивом рядків.

`callback`

Callback-функція, що викликається, якій буде переданий масив збіглих елементів з рядка `subject`. Callback-функція повинна повернути рядок із заміною. Callback-функція має бути описана так:

```methodsynopsis
handler(array $matches): string
```

Досить часто `callback` функція, окрім як у виклику \*\*pregreplacecallback()\*\*ні в чому більше не бере участі. Виходячи з цих міркувань, можна використовувати [анонімні функції](functions.anonymous.md) для створення callback-функції безпосередньо у виклику **pregreplacecallback()**. Якщо ви використовуєте такий підхід, вся інформація, пов'язана із заміною за регулярним виразом, буде зібрана в одному місці, і простір імен функцій не буде захаращуватися записами, що не використовуються.

**Приклад #1 **pregreplacecallback()** та анонімна функція**

```php
<?php
/* фильтр, подобный тому, что используется в системах Unix
 * для преобразования заглавных букв в начале параграфа в строчные */
$fp = fopen("php://stdin", "r") or die("не удалось прочесть stdin");
while (!feof($fp)) {
    $line = fgets($fp);
    $line = preg_replace_callback(
        '|<p>\s*\w|',
        function ($matches) {
            return strtolower($matches[0]);
        },
        $line
    );
    echo $line;
}
fclose($fp);
?>
```

`subject`

Рядок або масив рядків для пошуку та заміни.

`limit`

Максимально можлива кількість замін для кожного шаблону в кожному рядку `subject`. За замовчуванням одно `-1` (без обмежень).

`count`

Якщо зазначено, то ця змінна буде заповнена кількістю зроблених замін.

`flags`

`flags` може бути комбінацією прапорів **`PREG_OFFSET_CAPTURE`** і \*\*`PREG_UNMATCHED_AS_NULL`\*\*які впливають на формат масиву збігів. Дивіться опис у [pregmatch()](function.preg-match.md) для більш детальної інформації.

### Значення, що повертаються

**pregreplacecallback()** повертає масив, якщо параметр `subject` є масивом, інакше повертається рядок. У разі помилок повертається **`null`**

Якщо знайдено збіги, буде повернуто результуючий рядок, інакше `subject` повернеться незміненим.

### Помилки

Якщо переданий шаблон регулярного виразу не компілюється в допустимий регулярний вираз, видається помилка рівня **`E_WARNING`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Доданий параметр `flags` |

### Приклади

**Приклад #2 Приклад використання **pregreplacecallback()****

```php
<?php
// Этот текст был использован в 2002 году
// мы хотим обновить даты к 2003 году
$text = "День смеха был 01/04/2002\n";
$text.= "Последнее Рождество было 24/12/2001\n";
// callback-функция
function next_year($matches)
{
  // как обычно: $matches[0] -  полное вхождение шаблона
  // $matches[1] - вхождение первой подмаски,
  // заключённой в круглые скобки и так далее...
  return $matches[1].($matches[2]+1);
}
echo preg_replace_callback(
            "|(\d{2}/\d{2}/)(\d{4})|",
            "next_year",
            $text);

?>
```

Результат виконання цього прикладу:

```
День смеха был 01/04/2003
Последнее Рождество было 24/12/2002
```

**Приклад #3 Рекурсивна обробка BB-кодів за допомогою **pregreplacecallback()****

```php
<?php
$input = "верх [indent] глубже [indent] ещё глубже [/indent] глубже [/indent] верх";

function parseTagsRecursive($input)
{

    $regex = '#\[indent]((?:[^[]|\[(?!/?indent])|(?R))+)\[/indent]#';

    if (is_array($input)) {
        $input = '<div style="margin-left: 10px">'.$input[1].'</div>';
    }

    return preg_replace_callback($regex, 'parseTagsRecursive', $input);
}

$output = parseTagsRecursive($input);

echo $output;
?>
```

### Дивіться також

-   [Регулярні вирази PCRE](pcre.pattern.md)
-   [pregreplacecallbackarray()](function.preg-replace-callback-array.md) - Здійснює пошук та заміну за регулярним виразом з використанням функцій зворотного виклику
-   [pregquote()](function.preg-quote.md) - Екранує символи у регулярних виразах
-   [pregreplace()](function.preg-replace.md) - Виконує пошук та заміну за регулярним виразом
-   [preglasterror()](function.preg-last-error.md) - Повертає код помилки виконання останнього регулярного вираження PCRE
-   [Анонімні функції](functions.anonymous.md)
