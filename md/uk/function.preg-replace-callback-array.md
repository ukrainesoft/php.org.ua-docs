---
navigation:
  - function.preg-quote.md: « preg\_quote
  - function.preg-replace-callback.md: preg\_replace\_callback »
  - index.md: PHP Manual
  - ref.pcre.md: Функції PCRE
title: preg\_replace\_callback\_array
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# preg\_replace\_callback\_array

(PHP 7, PHP 8)

preg\_replace\_callback\_array — Здійснює пошук та заміну за регулярним виразом за допомогою функцій зворотного дзвінка.

### Опис

```methodsynopsis
preg_replace_callback_array(    array $pattern,    string|array $subject,    int $limit = -1,    int &$count = null,    int $flags = 0): string|array|null
```

Поведінка цієї функції схожа на [preg\_replace\_callback()](function.preg-replace-callback.md), за винятком того, що для кожного шаблону використовується своя функція зворотного дзвінка.

### Список параметрів

`pattern`

Асоціативний масив, що зв'язує шаблони регулярного вираження (ключі) та [callable](language.types.callable.md)(значения).

`subject`

Рядок, в якому буде здійснюватися пошук та заміна.

`limit`

Максимальна кількість замін для кожного шаблону в рядку `subject`По умолчанию`-1` (без обмежень).

`count`

Якщо заданий, то в зазначену змінну буде записано кількість зроблених замін.

`flags`

`flags` може бути комбінацією прапорів \*\*`PREG_OFFSET_CAPTURE`**и**`PREG_UNMATCHED_AS_NULL`\*\*які впливають на формат масиву збігів. Дивіться опис у [preg\_match()](function.preg-match.md) для більш детальної інформації.

### Значення, що повертаються

**preg\_replace\_callback\_array()** повертає масив, якщо параметр `subject` є масивом та рядок, якщо рядком. У разі виникнення помилки повертається **`null`**

Якщо збіги знайдені, буде повернуто новий рядок, а якщо ні, то вихідний `subject`

### Помилки

Якщо переданий шаблон регулярного виразу не компілюється в допустимий регулярний вираз, видається помилка рівня **`E_WARNING`**

### список змін

| Версия | Опис |
| --- | --- |
| 7.4.0 | Добавлен параметр`flags` |

### Приклади

**Пример #1 Пример использования**preg\_replace\_callback\_array()\*\*\*\*

```php
<?php
$subject = 'Aaaaaa Bbb';

preg_replace_callback_array(
    [
        '~[a]+~i' => function ($match) {
            echo 'Найдено ', strlen($match[0]), ' совпадений "a"', PHP_EOL;
        },
        '~[b]+~i' => function ($match) {
            echo 'Найдено ', strlen($match[0]), ' совпадений "b"', PHP_EOL;
        }
    ],
    $subject
);
?>
```

Результат виконання наведеного прикладу:

```
Найдено 6 совпадений "a"
Найдено 3 совпадений "b"
```

### Дивіться також

-   [Шаблони PCRE](pcre.pattern.md)
-   [preg\_replace\_callback()](function.preg-replace-callback.md) \- Виконує пошук за регулярним виразом та заміною з використанням callback-функції
-   [preg\_quote()](function.preg-quote.md) \- Екранує символи у регулярних виразах
-   [preg\_replace()](function.preg-replace.md) \- Виконує пошук та заміну за регулярним виразом
-   [preg\_last\_error()](function.preg-last-error.md) \- Повертає код помилки виконання останнього регулярного вираження PCRE
-   [Анонімні функції](functions.anonymous.md)
