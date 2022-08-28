Здійснює пошук та заміну за регулярним виразом з використанням функцій зворотного дзвінка

-   [« preg\_quote](function.preg-quote.html)
    
-   [preg\_replace\_callback »](function.preg-replace-callback.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PCRE](ref.pcre.html)
    
-   Здійснює пошук та заміну за регулярним виразом з використанням функцій зворотного дзвінка
    

# pregreplacecallbackarray

(PHP 7, PHP 8)

pregreplacecallbackarray — Здійснює пошук та заміну за регулярним виразом за допомогою функцій зворотного дзвінка.

### Опис

```methodsynopsis
preg_replace_callback_array(    array $pattern,    string|array $subject,    int $limit = -1,    int &$count = null,    int $flags = 0): string|array|null
```

Поведінка цієї функції схожа на [preg\_replace\_callback()](function.preg-replace-callback.html), за винятком того, що для кожного шаблону використовується функція зворотного дзвінка.

### Список параметрів

`pattern`

Асоціативний масив, що зв'язує шаблони регулярного вираження (ключі) та [callable](language.types.callable.html) (Значення).

`subject`

Рядок, в якому буде здійснюватися пошук та заміна.

`limit`

Максимальна кількість замін для кожного шаблону в рядку `subject`. За замовчуванням `-1` (без обмежень).

`count`

Якщо заданий, то в зазначену змінну буде записано кількість зроблених замін.

`flags`

`flags` може бути комбінацією прапорів **`PREG_OFFSET_CAPTURE`** і **`PREG_UNMATCHED_AS_NULL`**які впливають на формат масиву збігів. Дивіться опис у [preg\_match()](function.preg-match.html) для більш детальної інформації.

### Значення, що повертаються

**pregreplacecallbackarray()** повертає масив, якщо параметр `subject` є масивом та рядок, якщо рядком. У разі виникнення помилки повертається **`null`**

Якщо збіги знайдені, буде повернуто новий рядок, а якщо ні, то вихідний `subject`

### Помилки

Якщо переданий шаблон регулярного виразу не компілюється в допустимий регулярний вираз, видається помилка рівня **`E_WARNING`**

### список змін

| Версия | Описание                 |
|--------|--------------------------|
|        | Доданий параметр `flags` |

### Приклади

**Приклад #1 Приклад використання **pregreplacecallbackarray()****

```php
<?php
$subject = 'Aaaaaa Bbb';

preg_replace_callback_array(
    [
        '~[a]+~i' => function ($match) {
            echo 'Найдено ', strlen($match[0]), ' совпадений "a"', PHP_EOL;
        },
        '~[b]+~i' => function ($match) {
            echo 'Найдено ', strlen($match[0]), ' совпадений "b"', PHP_EOL;
        }
    ],
    $subject
);
?>
```

Результат виконання цього прикладу:

```
Найдено 6 совпадений "a"
Найдено 3 совпадений "b"
```

### Дивіться також

-   [Шаблоны PCRE](pcre.pattern.html)
-   [preg\_replace\_callback()](function.preg-replace-callback.html) - Виконує пошук за регулярним виразом та заміною з використанням callback-функції
-   [preg\_quote()](function.preg-quote.html) - Екранує символи у регулярних виразах
-   [preg\_replace()](function.preg-replace.html) - Виконує пошук та заміну за регулярним виразом
-   [preg\_last\_error()](function.preg-last-error.html) - Повертає код помилки виконання останнього регулярного вираження PCRE
-   [Анонимные функции](functions.anonymous.html)