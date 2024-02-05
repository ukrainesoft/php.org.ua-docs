---
navigation:
  - function.preg-filter.md: « preg\_filter
  - function.preg-last-error-msg.md: preg\_last\_error\_msg »
  - index.md: PHP Manual
  - ref.pcre.md: Функції PCRE
title: preg\_grep
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# preg\_grep

(PHP 4, PHP 5, PHP 7, PHP 8)

preg\_grep — Повертає масив входжень, які відповідають шаблону

### Опис

```methodsynopsis
preg_grep(string $pattern, array $array, int $flags = 0): array|false
```

Повертає масив, що складається з елементів вхідного масиву `array`, які відповідають заданому шаблону `pattern`

### Список параметрів

`pattern`

Шуканий шаблон у вигляді рядка.

`array`

Вхідний масив.

`flags`

В случае, если установлен в\*\*`PREG_GREP_INVERT`**, функция**preg\_grep()\*\* повертає ті елементи масиву, які *Не відповідає*заданному шаблону`pattern`

### Значення, що повертаються

Повертає масив, індексований ключами з масиву `array`или\*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо переданий шаблон регулярного виразу не компілюється в допустимий регулярний вираз, видається помилка рівня **`E_WARNING`**

### Приклади

**Пример #1 Пример использования**preg\_grep()\*\*\*\*

```php
<?php
// Возвращает все элементы массива,
// содержащие числа с плавающей точкой
$fl_array = preg_grep("/^(\d+)?\.\d+$/", $array);
?>
```

### Дивіться також

-   [Регулярні вирази PCRE](pcre.pattern.md)
-   [preg\_quote()](function.preg-quote.md) \- Екранує символи у регулярних виразах
-   [preg\_match\_all()](function.preg-match-all.md) \- Виконує глобальний пошук шаблону у рядку
-   [preg\_filter()](function.preg-filter.md) \- Здійснює пошук та заміну за регулярним виразом
-   [preg\_last\_error()](function.preg-last-error.md) \- Повертає код помилки виконання останнього регулярного вираження PCRE
