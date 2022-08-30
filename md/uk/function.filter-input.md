Приймає змінну ззовні PHP і, при необхідності, фільтрує її

-   [« filterinputarray](function.filter-input-array.html)
    
-   [filterlist »](function.filter-list.html)
    
-   [PHP Manual](index.html)
    
-   [Функції фільтрації даних](ref.filter.html)
    
-   Приймає змінну ззовні PHP і, при необхідності, фільтрує її
    

# filterinput

(PHP 5> = 5.2.0, PHP 7, PHP 8)

filterinput - Приймає змінну ззовні PHP і, при необхідності, фільтрує її

### Опис

```methodsynopsis
filter_input(    int $type,    string $var_name,    int $filter = FILTER_DEFAULT,    array|int $options = 0): mixed
```

### Список параметрів

`type`

Одна з констант **`INPUT_GET`** **`INPUT_POST`** **`INPUT_COOKIE`** **`INPUT_SERVER`** або **`INPUT_ENV`**

`var_name`

Ім'я змінної, що отримується.

`filter`

Ідентифікатор (ID) фільтра. На сторінці [Типи фільтрів](filter.filters.html) наведено список доступних фільтрів.

Якщо не вказано, то використовується **`FILTER_DEFAULT`**, який рівнозначний [**`FILTER_UNSAFE_RAW`**](filter.filters.sanitize.html). Це означає, що за замовчуванням не застосовується фільтр.

`options`

Асоціативний масив параметрів чи логічне АБО прапорів. Якщо фільтр приймає настройки, прапори можуть бути вказані в елементі масиву "flags".

### Значення, що повертаються

Значення запитуваної змінної у разі успішного виконання, **`false`**, якщо фільтрація завершилася невдачею, або **`null`**, якщо змінна `var_name` не визначена. Якщо встановлено прапор **`FILTER_NULL_ON_FAILURE`**, функція повертає **`false`**, якщо змінна не визначена та \*\*`null`\*\*якщо фільтрація завершилася невдачею.

### Приклади

**Приклад #1 Приклад використання **filterinput()****

```php
<?php
$search_html = filter_input(INPUT_GET, 'search', FILTER_SANITIZE_SPECIAL_CHARS);
$search_url = filter_input(INPUT_GET, 'search', FILTER_SANITIZE_ENCODED);
echo "Вы искали $search_html.\n";
echo "<a href='?search=$search_url'>Искать снова.</a>";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Вы искали Me &#38; son.
<a href='?search=Me%20%26%20son'>Искать снова.</a>
```

### Дивіться також

-   [filtervar()](function.filter-var.html) - Фільтрує змінну за допомогою певного фільтра
-   [filterinputarray()](function.filter-input-array.html) - Отримує кілька змінних ззовні PHP і, при необхідності, фільтрує їх
-   [filtervararray()](function.filter-var-array.html) - приймає кілька змінних і, при необхідності, фільтрує їх
-   [Типи фільтрів](filter.filters.html)