---
navigation:
  - function.stripos.md: « stripos
  - function.stristr.md: stristr »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: stripslashes
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stripslashes

(PHP 4, PHP 5, PHP 7, PHP 8)

stripslashes — Видаляє екранування символів

### Опис

```methodsynopsis
stripslashes(string $string): string
```

Видаляє екрануючі символи.

Функцию**stripslashes()** можна використовувати, якщо екранування символів не потрібне. Наприклад, дані не вставляють у базу даних, а просто виводяться в браузер.

### Список параметрів

`string`

Вхідний рядок.

### Значення, що повертаються

Повертає рядок із вирізаними зворотними слішами. (`\'`становится`'` і т.п.) Подвійні зворотні сліші (`\`) стають одинарними (`\`

### Приклади

**Пример #1 Пример использования**stripslashes()\*\*\*\*

```php
<?php
$str = "Ваc зовут O\'reilly?";

// выводит: Вас зовут O'reilly?
echo stripslashes($str);
?>
```

> **Зауваження** :
> 
> **stripslashes()** не рекурсивна. Якщо ви хочете застосувати її до багатовимірного масиву, вам необхідно використовувати рекурсивну функцію.

**Пример #2 Использование**stripslashes()\*\* з масивом\*\*

```php
<?php
function stripslashes_deep($value)
{
    $value = is_array($value) ?
                array_map('stripslashes_deep', $value) :
                stripslashes($value);

    return $value;
}

// Пример
$array = array("f\\'oo", "b\\'ar", array("fo\\'o", "b\\'ar"));
$array = stripslashes_deep($array);

// Вывод
print_r($array);
?>
```

Результат виконання наведеного прикладу:

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

-   [addslashes()](function.addslashes.md) \- Екранує рядок за допомогою слішів
-   [get\_magic\_quotes\_gpc()](function.get-magic-quotes-gpc.md) \- Отримання поточного значення конфігурації конфігурації magic\_quotes\_gpc
