Порівняння рядків із використанням алгоритму "natural order"

-   [« strnatcasecmp](function.strnatcasecmp.html)
    
-   [strncasecmp »](function.strncasecmp.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы со строками](ref.strings.html)
    
-   Порівняння рядків із використанням алгоритму "natural order"
    

# strnatcmp

(PHP 4, PHP 5, PHP 7, PHP 8)

strnatcmp - Порівняння рядків з використанням алгоритму "natural order"

### Опис

```methodsynopsis
strnatcmp(string $string1, string $string2): int
```

Ця функція реалізує алгоритм порівняння, який упорядковує алфавітно-цифрові рядки подібно до того, як це зробив би людина, такий алгоритм називається "natural ordering". Порівняння відбувається з урахуванням регістру.

### Список параметрів

`string1`

Перший рядок.

`string2`

Другий рядок.

### Значення, що повертаються

Подібно до інших функцій порівняння рядків, ця функція повертає від'ємне число, якщо `string1` менше ніж `string2`, позитивне число, якщо `string1` більше ніж `string2`, та 0 якщо рядки рівні.

### Приклади

Приклад, що показує відмінність цього алгоритму від звичайних функцій порівняння (використовуються в [strcmp()](function.strcmp.html)), наведений нижче:

```php
<?php
$arr1 = $arr2 = array("img12.png", "img10.png", "img2.png", "img1.png");
echo "Стандартный алгоритм сравнения\n";
usort($arr1, "strcmp");
print_r($arr1);
echo "\nАлгоритм \"natural order\"\n";
usort($arr2, "strnatcmp");
print_r($arr2);
?>
```

Результат виконання цього прикладу:

```
Стандартный алгоритм сравнения
Array
(
    [0] => img1.png
    [1] => img10.png
    [2] => img12.png
    [3] => img2.png
)

Алгоритм "natural order"
Array
(
    [0] => img1.png
    [1] => img2.png
    [2] => img10.png
    [3] => img12.png
)
```

Для отримання додаткової інформації дивіться [» Natural Order String Comparison](https://github.com/sourcefrog/natsort)

### Дивіться також

-   [preg\_match()](function.preg-match.html) - Виконує перевірку на відповідність регулярному виразу
-   [strcasecmp()](function.strcasecmp.html) - Бінарно-безпечне порівняння рядків без урахування регістру
-   [substr()](function.substr.html) - Повертає підрядок
-   [stristr()](function.stristr.html) - Реєстронезалежний варіант функції strstr
-   [strcmp()](function.strcmp.html) - Бінарно-безпечне порівняння рядків
-   [strncmp()](function.strncmp.html) - Бінарно-безпечне порівняння перших n символів рядків
-   [strncasecmp()](function.strncasecmp.html) - Бінарно-безпечне порівняння перших n символів рядків без урахування регістру
-   [strnatcasecmp()](function.strnatcasecmp.html) - Порівняння рядків без урахування регістру з використанням алгоритму "natural order"
-   [strstr()](function.strstr.html) - Знаходить перше входження підрядка
-   [natsort()](function.natsort.html) - Сортує масив, використовуючи алгоритм "natural order"
-   [natcasesort()](function.natcasesort.html) - Сортує масив, використовуючи алгоритм "natural order" без урахування регістру символів