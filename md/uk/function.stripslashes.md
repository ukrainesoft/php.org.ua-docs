Видаляє екранування символів

-   [« stripos](function.stripos.html)
    
-   [stristr »](function.stristr.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы со строками](ref.strings.html)
    
-   Видаляє екранування символів
    

# stripslashes

(PHP 4, PHP 5, PHP 7, PHP 8)

stripslashes — Видаляє екранування символів

### Опис

```methodsynopsis
stripslashes(string $string): string
```

Видаляє екрануючі символи.

функцію **stripslashes()** можна використовувати, якщо екранування символів не потрібне. Наприклад, дані не вставляють у базу даних, а просто виводяться в браузер.

### Список параметрів

`string`

Вхідний рядок.

### Значення, що повертаються

Повертає рядок із вирізаними зворотними слішами. (`\'` стає `'` і т.п.) Подвійні зворотні сліші (`\\`) стають одинарними (`\`

### Приклади

**Приклад #1 Приклад використання **stripslashes()****

```php
<?php
$str = "Ваc зовут O\'reilly?";

// выводит: Вас зовут O'reilly?
echo stripslashes($str);
?>
```

> **Зауваження**
> 
> **stripslashes()** не рекурсивна. Якщо ви хочете застосувати її до багатовимірного масиву, вам необхідно використовувати рекурсивну функцію.

**Приклад #2 Використання **stripslashes()** з масивом**

```php
<?php
function stripslashes_deep($value)
{
    $value = is_array($value) ?
                array_map('stripslashes_deep', $value) :
                stripslashes($value);

    return $value;
}

// Пример
$array = array("f\\'oo", "b\\'ar", array("fo\\'o", "b\\'ar"));
$array = stripslashes_deep($array);

// Вывод
print_r($array);
?>
```

Результат виконання цього прикладу:

```
Array
(
    [0] => f'oo
    [1] => b'ar
    [2] => Array
        (
            [0] => fo'o
            [1] => b'ar
        )

)
```

### Дивіться також

-   [addslashes()](function.addslashes.html) - Екранує рядок за допомогою слішів
-   [get\_magic\_quotes\_gpc()](function.get-magic-quotes-gpc.html) - Отримання поточного значення конфігурації конфігурації magicquotesgpc